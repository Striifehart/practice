--
-- PostgreSQL database dump
--

-- Dumped from database version 12.17 (Ubuntu 12.17-1.pgdg22.04+1)
-- Dumped by pg_dump version 12.17 (Ubuntu 12.17-1.pgdg22.04+1)

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

DROP DATABASE universe;
--
-- Name: universe; Type: DATABASE; Schema: -; Owner: freecodecamp
--

CREATE DATABASE universe WITH TEMPLATE = template0 ENCODING = 'UTF8' LC_COLLATE = 'C.UTF-8' LC_CTYPE = 'C.UTF-8';


ALTER DATABASE universe OWNER TO freecodecamp;

\connect universe

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

SET default_tablespace = '';

SET default_table_access_method = heap;

--
-- Name: event; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.event (
    event_id integer NOT NULL,
    name character varying NOT NULL,
    event_type character varying,
    event_date date,
    location character varying,
    participants integer
);


ALTER TABLE public.event OWNER TO freecodecamp;

--
-- Name: event_event_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.event_event_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.event_event_id_seq OWNER TO freecodecamp;

--
-- Name: event_event_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.event_event_id_seq OWNED BY public.event.event_id;


--
-- Name: galaxy; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.galaxy (
    galaxy_id integer NOT NULL,
    name character varying NOT NULL,
    size_in_km numeric,
    has_black_hole boolean,
    classification text,
    num_stars integer
);


ALTER TABLE public.galaxy OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.galaxy_galaxy_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.galaxy_galaxy_id_seq OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.galaxy_galaxy_id_seq OWNED BY public.galaxy.galaxy_id;


--
-- Name: moon; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.moon (
    moon_id integer NOT NULL,
    name character varying NOT NULL,
    planet_id integer,
    size_in_km numeric,
    is_inhabited boolean,
    distance_from_planet numeric
);


ALTER TABLE public.moon OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.moon_moon_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.moon_moon_id_seq OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.moon_moon_id_seq OWNED BY public.moon.moon_id;


--
-- Name: planet; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.planet (
    planet_id integer NOT NULL,
    name character varying NOT NULL,
    star_id integer,
    type character varying,
    radius numeric,
    has_moons boolean
);


ALTER TABLE public.planet OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.planet_planet_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.planet_planet_id_seq OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.planet_planet_id_seq OWNED BY public.planet.planet_id;


--
-- Name: star; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.star (
    star_id integer NOT NULL,
    name character varying NOT NULL,
    galaxy_id integer,
    type character varying,
    mass numeric,
    is_binary boolean
);


ALTER TABLE public.star OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.star_star_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.star_star_id_seq OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.star_star_id_seq OWNED BY public.star.star_id;


--
-- Name: event event_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.event ALTER COLUMN event_id SET DEFAULT nextval('public.event_event_id_seq'::regclass);


--
-- Name: galaxy galaxy_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy ALTER COLUMN galaxy_id SET DEFAULT nextval('public.galaxy_galaxy_id_seq'::regclass);


--
-- Name: moon moon_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon ALTER COLUMN moon_id SET DEFAULT nextval('public.moon_moon_id_seq'::regclass);


--
-- Name: planet planet_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet ALTER COLUMN planet_id SET DEFAULT nextval('public.planet_planet_id_seq'::regclass);


--
-- Name: star star_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star ALTER COLUMN star_id SET DEFAULT nextval('public.star_star_id_seq'::regclass);


--
-- Data for Name: event; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.event VALUES (1, 'Supernova 1987A', 'Supernova', '1987-02-23', 'Large Magellanic Cloud', 500);
INSERT INTO public.event VALUES (2, 'Solar Eclipse 2017', 'Solar Eclipse', '2017-08-21', 'United States', 10000);
INSERT INTO public.event VALUES (3, 'Halley''s Comet 1986', 'Comet', '1986-03-14', 'Solar System', 100000000);
INSERT INTO public.event VALUES (4, 'Perseid Meteor Shower 2023', 'Meteor Shower', '2023-08-12', 'Northern Hemisphere', 1000000);
INSERT INTO public.event VALUES (5, 'Transit of Venus 2012', 'Astronomical Transit', '2012-06-05', 'Earth', 2000);
INSERT INTO public.event VALUES (6, 'Hale-Bopp Comet 1997', 'Comet', '1997-03-21', 'Solar System', 10000000);


--
-- Data for Name: galaxy; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.galaxy VALUES (1, 'Milky Way', 100000, true, 'Spiral', 400);
INSERT INTO public.galaxy VALUES (2, 'Andromeda', 120000, true, 'Spiral', 500);
INSERT INTO public.galaxy VALUES (3, 'Whirlpool', 80000, false, 'Spiral', 200);
INSERT INTO public.galaxy VALUES (4, 'Sombrero', 90000, false, 'Spiral', 250);
INSERT INTO public.galaxy VALUES (5, 'Triangulum', 70000, false, 'Irregular', 150);
INSERT INTO public.galaxy VALUES (6, 'Cartwheel', 75000, false, 'Ring', 180);


--
-- Data for Name: moon; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.moon VALUES (1, 'Moon', 1, 3474.8, false, 384400);
INSERT INTO public.moon VALUES (2, 'Phobos', 2, 22.4, false, 9376);
INSERT INTO public.moon VALUES (3, 'Deimos', 2, 12.4, false, 23460);
INSERT INTO public.moon VALUES (4, 'Europa', 3, 1560.8, false, 671100);
INSERT INTO public.moon VALUES (5, 'Ganymede', 3, 5262.4, false, 1070400);
INSERT INTO public.moon VALUES (6, 'Titan', 4, 5150, false, 1221860);
INSERT INTO public.moon VALUES (7, 'Enceladus', 4, 252.1, false, 237948);
INSERT INTO public.moon VALUES (8, 'Miranda', 5, 471.6, false, 129390);
INSERT INTO public.moon VALUES (9, 'Triton', 6, 2706.8, false, 354759);
INSERT INTO public.moon VALUES (10, 'Dagobah', 7, 856.9, false, 17500);
INSERT INTO public.moon VALUES (11, 'Alderaan Moon 1', 8, 1473, false, 17000);
INSERT INTO public.moon VALUES (12, 'Alderaan Moon 2', 8, 1545, false, 22000);
INSERT INTO public.moon VALUES (13, 'Krypton Moon 1', 9, 1218, false, 19000);
INSERT INTO public.moon VALUES (14, 'Krypton Moon 2', 9, 1300, false, 22000);
INSERT INTO public.moon VALUES (15, 'Vulcan Moon 1', 10, 1579, false, 15000);
INSERT INTO public.moon VALUES (16, 'Vulcan Moon 2', 10, 1698, false, 20000);
INSERT INTO public.moon VALUES (17, 'Hoth Moon 1', 11, 856.9, false, 17500);
INSERT INTO public.moon VALUES (18, 'Hoth Moon 2', 11, 789.1, false, 16000);
INSERT INTO public.moon VALUES (19, 'Endor Moon 1', 12, 1234.5, false, 19000);
INSERT INTO public.moon VALUES (20, 'Endor Moon 2', 12, 1350.3, false, 22000);


--
-- Data for Name: planet; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.planet VALUES (1, 'Earth', 1, 'Terrestrial', 6371, true);
INSERT INTO public.planet VALUES (2, 'Mars', 1, 'Terrestrial', 3389.5, true);
INSERT INTO public.planet VALUES (3, 'Jupiter', 1, 'Gas giant', 69911, true);
INSERT INTO public.planet VALUES (4, 'Saturn', 1, 'Gas giant', 58232, true);
INSERT INTO public.planet VALUES (5, 'Uranus', 1, 'Ice giant', 25362, true);
INSERT INTO public.planet VALUES (6, 'Neptune', 1, 'Ice giant', 24622, true);
INSERT INTO public.planet VALUES (7, 'Tatooine', 6, 'Terrestrial', 10120, true);
INSERT INTO public.planet VALUES (8, 'Alderaan', 6, 'Terrestrial', 12120, true);
INSERT INTO public.planet VALUES (9, 'Krypton', 6, 'Terrestrial', 9518, true);
INSERT INTO public.planet VALUES (10, 'Vulcan', 6, 'Terrestrial', 11604, true);
INSERT INTO public.planet VALUES (11, 'Hoth', 6, 'Terrestrial', 7200, true);
INSERT INTO public.planet VALUES (12, 'Endor', 6, 'Terrestrial', 4900, true);


--
-- Data for Name: star; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.star VALUES (1, 'Sun', 1, 'G-type main-sequence', 1989000000000000000000000000000, false);
INSERT INTO public.star VALUES (2, 'Sirius', 1, 'A-type main-sequence', 2020000000000000000000000000000, true);
INSERT INTO public.star VALUES (3, 'Alpha Centauri A', 1, 'G-type main-sequence', 2200000000000000000000000000000, false);
INSERT INTO public.star VALUES (4, 'Alpha Centauri B', 1, 'K-type main-sequence', 1680000000000000000000000000000, false);
INSERT INTO public.star VALUES (5, 'Proxima Centauri', 1, 'M-type main-sequence', 123000000000000000000000000000, false);
INSERT INTO public.star VALUES (6, 'Betelgeuse', 2, 'Red supergiant', 11600000000000000000000000000000, false);


--
-- Name: event_event_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.event_event_id_seq', 6, true);


--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.galaxy_galaxy_id_seq', 6, true);


--
-- Name: moon_moon_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.moon_moon_id_seq', 20, true);


--
-- Name: planet_planet_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.planet_planet_id_seq', 12, true);


--
-- Name: star_star_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.star_star_id_seq', 6, true);


--
-- Name: event event_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.event
    ADD CONSTRAINT event_name_key UNIQUE (name);


--
-- Name: event event_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.event
    ADD CONSTRAINT event_pkey PRIMARY KEY (event_id);


--
-- Name: galaxy galaxy_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_name_key UNIQUE (name);


--
-- Name: galaxy galaxy_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_pkey PRIMARY KEY (galaxy_id);


--
-- Name: moon moon_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_name_key UNIQUE (name);


--
-- Name: moon moon_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_pkey PRIMARY KEY (moon_id);


--
-- Name: planet planet_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_name_key UNIQUE (name);


--
-- Name: planet planet_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_pkey PRIMARY KEY (planet_id);


--
-- Name: star star_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_name_key UNIQUE (name);


--
-- Name: star star_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_pkey PRIMARY KEY (star_id);


--
-- Name: moon moon_planet_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_planet_id_fkey FOREIGN KEY (planet_id) REFERENCES public.planet(planet_id);


--
-- Name: planet planet_star_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_star_id_fkey FOREIGN KEY (star_id) REFERENCES public.star(star_id);


--
-- Name: star star_galaxy_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_galaxy_id_fkey FOREIGN KEY (galaxy_id) REFERENCES public.galaxy(galaxy_id);


--
-- PostgreSQL database dump complete
--


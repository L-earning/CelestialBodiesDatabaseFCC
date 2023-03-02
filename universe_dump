--
-- PostgreSQL database dump
--

-- Dumped from database version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)
-- Dumped by pg_dump version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)

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
-- Name: asteroid; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.asteroid (
    asteroid_id integer NOT NULL,
    name character varying(60) NOT NULL,
    distance_from_earth_in_km integer,
    galaxy_id integer
);


ALTER TABLE public.asteroid OWNER TO freecodecamp;

--
-- Name: asteroid_asteriod_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.asteroid_asteriod_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.asteroid_asteriod_id_seq OWNER TO freecodecamp;

--
-- Name: asteroid_asteriod_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.asteroid_asteriod_id_seq OWNED BY public.asteroid.asteroid_id;


--
-- Name: galaxy; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.galaxy (
    galaxy_id integer NOT NULL,
    name character varying(60) NOT NULL,
    age_in_millions_of_years numeric NOT NULL,
    description text,
    has_life boolean
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
    name character varying(60) NOT NULL,
    age_in_millions_of_years numeric NOT NULL,
    description text,
    planet_id integer
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
    name character varying(60) NOT NULL,
    age_in_millions_of_years numeric NOT NULL,
    diameter_in_km integer NOT NULL,
    description text,
    has_life boolean,
    star_id integer,
    galaxy_id integer
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
    name character varying(60) NOT NULL,
    age_in_millions_of_years numeric NOT NULL,
    diameter_in_km integer NOT NULL,
    description text,
    galaxy_id integer
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
-- Name: asteroid asteroid_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.asteroid ALTER COLUMN asteroid_id SET DEFAULT nextval('public.asteroid_asteriod_id_seq'::regclass);


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
-- Data for Name: asteroid; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.asteroid VALUES (1, '4 Vesta', 492472313, 1);
INSERT INTO public.asteroid VALUES (2, '3 Juno', 380771445, 1);
INSERT INTO public.asteroid VALUES (3, '2 Pallas', 228860913, 1);


--
-- Data for Name: galaxy; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.galaxy VALUES (1, 'Milky Way', 13600000000, 'The galaxy that our solar system and our planet - Earth - is in', true);
INSERT INTO public.galaxy VALUES (2, 'Andromeda', 10010000000, 'The nearest largest galaxy to the Milky Way', NULL);
INSERT INTO public.galaxy VALUES (3, 'Cigar galaxy', 13300000000, 'Around the center, starts are born 10 times faster than in the Milky Way', NULL);
INSERT INTO public.galaxy VALUES (4, 'Messier 81', 13300000000, 'One of the brightest galaxies in the night sky', NULL);
INSERT INTO public.galaxy VALUES (5, 'Sombrero galaxy', 13250000000, 'The center is supposidly a black hole', NULL);
INSERT INTO public.galaxy VALUES (6, 'Whirlpool galaxy', 400300000, 'Has been highly studies and observed', NULL);


--
-- Data for Name: moon; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.moon VALUES (1, 'The Moon', 4527, 'The moon orbiting the Earth', 1);
INSERT INTO public.moon VALUES (2, 'Io', 4500, 'One of many moons orbiting Jupiter', 5);
INSERT INTO public.moon VALUES (3, 'Europa', 4500, 'OG Jupiter moon', 5);
INSERT INTO public.moon VALUES (4, 'Ganymede', 4500, 'OG Jupiter moon', 5);
INSERT INTO public.moon VALUES (5, 'Callisto', 4500, 'OG Jupiter moon', 5);
INSERT INTO public.moon VALUES (6, 'Adrastea', 4500, 'Another Jupiter moon', 5);
INSERT INTO public.moon VALUES (7, 'Aitne', 4500, 'One of many moons orbiting Jupiter', 5);
INSERT INTO public.moon VALUES (8, 'Amalthea', 4500, 'Jupiter moon', 5);
INSERT INTO public.moon VALUES (9, 'Ananke', 4500, 'Jupiter moon', 5);
INSERT INTO public.moon VALUES (10, 'Arche', 4500, 'Jupiter moon', 5);
INSERT INTO public.moon VALUES (11, 'Carpo', 4500, 'Another Jupiter moon', 5);
INSERT INTO public.moon VALUES (12, 'Dia', 4500, 'One of many moons orbiting Jupiter', 5);
INSERT INTO public.moon VALUES (13, 'Elara', 4500, 'Jupiter moon', 5);
INSERT INTO public.moon VALUES (14, 'Ersa', 4500, 'Jupiter moon', 5);
INSERT INTO public.moon VALUES (15, 'Helike', 4500, 'Jupiter moon', 5);
INSERT INTO public.moon VALUES (16, 'Herse', 4500, 'Another Jupiter moon', 5);
INSERT INTO public.moon VALUES (17, 'Sponde', 4500, 'One of many moons orbiting Jupiter', 5);
INSERT INTO public.moon VALUES (18, 'Pandia', 4500, 'Jupiter moon', 5);
INSERT INTO public.moon VALUES (19, 'Metis', 4500, 'Jupiter moon', 5);
INSERT INTO public.moon VALUES (20, 'Leda', 4500, 'Jupiter moon', 5);
INSERT INTO public.moon VALUES (21, 'Kale', 4500, 'Another Jupiter moon', 5);
INSERT INTO public.moon VALUES (22, 'Cyllene', 4500, 'One of many moons orbiting Jupiter', 5);
INSERT INTO public.moon VALUES (23, 'Isonoe', 4500, 'Jupiter moon', 5);
INSERT INTO public.moon VALUES (24, 'Kalyte', 4500, 'Jupiter moon', 5);
INSERT INTO public.moon VALUES (25, 'Megaclite', 4500, 'Jupiter moon', 5);
INSERT INTO public.moon VALUES (26, 'Thebe', 4500, 'Another Jupiter moon', 5);


--
-- Data for Name: planet; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.planet VALUES (1, 'Earth', 4540, 12756, 'the planet we live on', true, 1, 1);
INSERT INTO public.planet VALUES (2, 'Mercury', 4540, 4879, 'tiny', false, 1, 1);
INSERT INTO public.planet VALUES (3, 'Venus', 4540, 12104, 'Named after greek goddess', false, 1, 1);
INSERT INTO public.planet VALUES (4, 'Mars', 4540, 6779, 'Red planet', true, 1, 1);
INSERT INTO public.planet VALUES (5, 'Jupiter', 4540, 143000, 'Has many moons', false, 1, 1);
INSERT INTO public.planet VALUES (6, 'Saturn', 4540, 116460, 'Known for its rings', false, 1, 1);
INSERT INTO public.planet VALUES (7, 'Uranus', 4540, 50724, 'Funny name', false, 1, 1);
INSERT INTO public.planet VALUES (8, 'Neptune', 4540, 49224, 'Blue planet other than Earth', false, 1, 1);
INSERT INTO public.planet VALUES (9, 'Pluto', 4540, 2370, 'Best planet - I am aware it is a dwarf planet', false, 1, 1);
INSERT INTO public.planet VALUES (10, 'Kepler-186f', 4000, 14908, 'Second Earth', true, NULL, 1);
INSERT INTO public.planet VALUES (11, 'Imagine', 6000, 76033, 'An imaginary planet', false, 2, 1);
INSERT INTO public.planet VALUES (12, 'Believe', 7381, 237220, 'Believe that this planet exist, i am too tired to research', true, 4, 1);


--
-- Data for Name: star; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.star VALUES (1, 'The sun', 4500, 1400000, 'The main star in our solar system', 1);
INSERT INTO public.star VALUES (2, 'Sirius', 230, 2400000, 'Brightest star in the night sky', 1);
INSERT INTO public.star VALUES (3, 'VV Cephei', 25, 264000000, 'Biggest star in the milky way', 1);
INSERT INTO public.star VALUES (4, 'Rigel', 8, 109781500, 'rightest star in Orion', 1);
INSERT INTO public.star VALUES (5, 'Pollux', 725, 12244000, 'Brightest star in Gemini', 1);
INSERT INTO public.star VALUES (6, 'Antares', 11, 946150000, 'Brightest star in Gemini', 1);


--
-- Name: asteroid_asteriod_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.asteroid_asteriod_id_seq', 3, true);


--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.galaxy_galaxy_id_seq', 1, false);


--
-- Name: moon_moon_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.moon_moon_id_seq', 26, true);


--
-- Name: planet_planet_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.planet_planet_id_seq', 1, false);


--
-- Name: star_star_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.star_star_id_seq', 1, false);


--
-- Name: asteroid asteroid_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.asteroid
    ADD CONSTRAINT asteroid_pkey PRIMARY KEY (asteroid_id);


--
-- Name: asteroid astroid_unq; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.asteroid
    ADD CONSTRAINT astroid_unq UNIQUE (name);


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
-- Name: asteroid asteroid_galaxy_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.asteroid
    ADD CONSTRAINT asteroid_galaxy_id_fkey FOREIGN KEY (galaxy_id) REFERENCES public.galaxy(galaxy_id);


--
-- Name: moon moon_planet_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_planet_id_fkey FOREIGN KEY (planet_id) REFERENCES public.planet(planet_id);


--
-- Name: planet planet_galaxy_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_galaxy_id_fkey FOREIGN KEY (galaxy_id) REFERENCES public.galaxy(galaxy_id);


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


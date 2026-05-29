# CinemaScope AI

CinemaScope AI is an ASP.NET Core MVC web application for managing movies, actors, and actor-movie relationships while using AI to generate movie reviews and actor commentary. The application combines CRUD functionality, Azure-hosted services, sentiment analysis, and database-backed media storage into a movie management platform.

## Overview

This project was created as a movie and actor management website with AI-generated reviews for movies and AI-generated Twitter-style comments for actors. The application includes full CRUD functionality for movies, actors, and actor-movie relationships, along with sentiment analysis powered by VaderSharp2 and AI-generated content powered by Azure.AI.OpenAI.

## Features

- Home page with an introduction to the site
- Full CRUD functionality for movies
- Full CRUD functionality for actors
- Full CRUD functionality for actor-movie relationships
- Movie records include:
  - Title
  - IMDb hyperlink
  - Genre
  - Year of release
  - Poster stored as `byte[]` in the database
- Actor records include:
  - Name
  - Gender
  - Age
  - IMDb hyperlink
  - Photo stored as `byte[]` in the database

## Movie Details Features

Each movie details page includes:

- A list of actors in the selected movie
- Five AI-generated movie reviews created from a single OpenAI API call and then parsed for display
- Sentiment analysis for each generated review using VaderSharp2
- A heading showing the average overall sentiment for the selected movie

## Actor Details Features

Each actor details page includes:

- A list of movies associated with the selected actor
- Ten AI-generated Twitter-style comments created from a single OpenAI API call and then parsed for display
- Sentiment analysis for each generated comment using VaderSharp2
- A heading showing the overall sentiment for the selected actor

## Technologies Used

- ASP.NET Core MVC
- C#
- Entity Framework Core
- Azure.AI.OpenAI
- VaderSharp2
- Azure SQL Database
- Azure App Service

## Project Requirements Implemented

- ASP.NET Core Web Application (Model-View-Controller) using C#
- Individual Authentication (in-app)
- Use of the `Azure.AI.OpenAI` NuGet package
- Use of the `VaderSharp2` NuGet package
- At least four movies stored in the database
- At least eight actors stored in the database
- Separate HTML, CSS, and JavaScript files
- Use of view models instead of `ViewData` or `ViewBag
- Use of SRI hashes for externally linked resources
- Use of Secrets Manager for API keys and database credentials
- Safe behavior for deletes and duplicate relationship prevention
- No console errors, broken links, or runtime issues

## Database and Deployment

The application is designed to use an Azure SQL Database configured through Azure for Students, with SQL authentication and firewall rules configured for development access. The site is published through Azure App Service, and deployment-side secrets are added as Azure environment variables after publishing.

# Project Overview: Holocron Scrolls

## Project Vision
Provide the best way to track and find Star Wars Novels / Books.

## Project Mission/Purpose Key Goals/Objectives
- [ ] Find Star Wars Books.
- [ ] Visualize and keep Track of your own collection.
- [ ] Provide an interactive map which is essentially a timeline of the Star Wars universe with the Star Wars books.

## Scope Definition

### In Scope:
What are the major deliverables, functionalities, or areas this project will cover?
- [ ] **Library of Star Wars Books (Epic 1):** Creation of a comprehensive database of Star Wars books, including metadata such as title, author, publication date, series, era, cover art, and a short description. This does not include the actual content of the books.
    - *Link to detailed spec: [Holocron_Scrolls_Epic1_Library_Spec.md](Holocron_Scrolls_Epic1_Library_Spec.md) (To be created)*
- [ ] **Personal Collection Tracking (Epic 2):** Allow users to create accounts and manage their personal collection of Star Wars books. Users should be able to mark books as owned, read, wishlisted, etc.
    - *Link to detailed spec: [Holocron_Scrolls_Epic2_Collection_Tracking_Spec.md](Holocron_Scrolls_Epic2_Collection_Tracking_Spec.md) (To be created)*
- [ ] **Interactive Star Wars Novels Timeline (Epic 3):** Develop an interactive visual timeline of the Star Wars universe where books are placed according to their in-universe chronological order. Users should be able to filter and navigate this timeline.
    - *Link to detailed spec: [Holocron_Scrolls_Epic3_Interactive_Timeline_Spec.md](Holocron_Scrolls_Epic3_Interactive_Timeline_Spec.md) (To be created)*

### Out of Scope:
What will this project explicitly not include?
-   The actual digital content or e-reader functionality for the Star Wars books.
-   User reviews and rating systems (initially).
-   Social networking features beyond basic collection sharing (if implemented).
-   Support for languages other than English (initially).
-   Selling or facilitating the sale of books.
-   Mobile native applications (beyond the web application's responsiveness).

## Target Audience/Users
Star Wars Book Readers, collectors, and enthusiasts who want to explore the timeline and manage their reading progress.

## Assumptions
- [ ] Users have a basic understanding of the Star Wars universe and its timeline.
- [ ] Sufficient and accurate Star Wars book data (metadata, chronological order) can be sourced or compiled.
- [ ] Users will be willing to manually input their book collections.
- [ ] The chosen technology stack will be suitable for the project's performance and scalability needs.
- [ ] Team members have or can acquire the necessary skills for the selected technology stack.

## Constraints & Potential Risks
- [ ] **Data Acquisition and Accuracy:** Sourcing comprehensive and accurate data for all Star Wars books, including their correct chronological placement, can be challenging and time-consuming.
- [ ] **Scope Creep:** The vastness of the Star Wars universe and potential feature requests could lead to expanding the project beyond its initial defined scope.
- [ ] **User Interface Complexity:** Designing an intuitive and user-friendly interface for the interactive timeline and collection management could be complex.
- [ ] **Third-Party API Reliance (if any):** If external APIs are used for book data, reliance on their availability and terms of service could pose a risk.
- [ ] **Performance of Blazor WASM:** Ensuring smooth performance for the interactive timeline, especially with a large dataset, on various devices.
- [ ] **Copyright and IP:** Ensuring that the use of book titles, cover art (thumbnails), and other metadata complies with copyright laws.

## Technology Stack Considerations

### Backend
-   **Framework:** ASP.NET Core 9 Controller API
-   **ORM:** Entity Framework Core
-   **Testing:** MS Test for Unit Tests
-   **Additional Libraries:**
    -   [ ] Consider MediatR for implementing CQRS pattern (separating commands and queries).
    -   [ ] Consider FluentValidation for robust request validation.
    -   [ ] Consider AutoMapper for object-to-object mapping.
    -   [ ] Consider Serilog or NLog for structured logging.
    -   [ ] Explore options for background tasks if data fetching/processing is intensive (e.g., Hangfire).

### Frontend
-   **Framework:** Blazor WebAssembly (WASM)
-   **UI Components:**
    -   [ ] Consider a Blazor component library like MudBlazor, Blazorise, or Radzen Blazor Components to speed up UI development.

### Database
-   SQLite (Simple, file-based, good for development and smaller applications)

## Milestones
- [ ] **M1: Project Setup & Core Backend (Date: TBD)**
    - [ ] Initialize Git repository and define branching strategy.
    - [ ] Setup basic CI (Continuous Integration) Pipeline.
    - [ ] Setup backend solution structure (API, Core/Domain, Application, Infrastructure/Persistence, Tests).
    - [ ] Define initial database schema with EF Core for `Book` entity.
    - [ ] Implement basic CRUD APIs for Book metadata.
    - [ ] Write initial unit tests for CRUD operations.
- [ ] **M2: Basic Book Library Frontend (Date: TBD)**
    - [ ] Setup Blazor WASM project.
    - [ ] Create UI to display a list of books from the backend.
    - [ ] Implement basic search and filtering for books.
- [ ] **M3: User Accounts & Personal Collection - Phase 1 (Date: TBD)**
    - [ ] Implement user registration and login (ASP.NET Core Identity).
    - [ ] Allow users to add/remove books to their "Owned" collection.
- [ ] **M4: Interactive Timeline - Phase 1 (Date: TBD)**
    - [ ] Design data structure for timeline events/book placements.
    - [ ] Implement basic rendering of books on a chronological timeline.
- [ ] **M5: Advanced Collection Features & Timeline Interactivity (Date: TBD)**
    - [ ] Add more collection statuses (Read, Wishlist).
    - [ ] Implement filtering and navigation on the interactive timeline.
- [ ] **M6: Beta Testing & Refinement (Date: TBD)**
- [ ] **M7: Production Deployment (Date: TBD)**

## Immediate Action Items
- [ ] Define initial database schema for the `Book` entity in detail (see M1 details).
- [ ] Research and select a Blazor UI component library.
- [ ] Begin sourcing and compiling Star Wars book metadata and chronological order.
- [ ] Set up the Git repository for the project (see M1 details).
- [ ] Schedule a meeting to discuss initial sprint goals for M1.
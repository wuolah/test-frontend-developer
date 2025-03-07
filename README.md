# Technical test for frontend developers – Event Attendance 🎫

## Introduction 👋

Welcome to Wuolah’s technical test for frontend developers.  
We want to evaluate how you solve a practical case that simulates the challenges of building user interfaces in the academic environment.

## The test 📝

### Basic requirements

Develop a user interface for managing event attendance, implementing the following functionalities:

1. **List events:**  
   _As a user, I want to view a list of available events_ (e.g., music festivals, conferences, fairs, etc.). 🎉

2. **Event details:**  
   _As a user, I want to view the details of a specific event_, including title, description, date, and location. 📅

   _As a user, I want to view a countdown timer that updates in real-time until the event date_, so that I can easily track how much time remains before the event starts. 🕙

4. **Mark/Change attendance:**  
   _As a user, I want to confirm my attendance at an event_ and, if necessary, cancel or update my attendance. 👍/👎

5. **List attendees:**  
   _As a user, I want to see a list of users who have confirmed attendance for a specific event._ 👥

Use this project template (React + Next.js) and any tools you typically use in a real-world application.

### Bonus ✨

- The event details view should display a countdown timer. 
- The interface should display a reminder notification to users who have confirmed attendance one week before the event. Please provide your theoretical approach on how you would implement this processing (implementation is not required).

### API

You can use the following events API: `https://67c888390acf98d07086f189.mockapi.io/api/v1`

<details>
  <summary><b>Create user</b></summary>

Endpoint: `POST /user`

Code example:

```javascript
const res = await fetch(
  "https://67c888390acf98d07086f189.mockapi.io/api/v1/user",
  {
    method: "POST",
    headers: { "content-type": "application/json" },
    body: JSON.stringify({
      username: "your_preferred_username",
      avatarUrl:
        "https://cdn.wuolahservices.com/users/default/avatar/v1/avatar-1-big.jpg",
    }),
  }
);
const user = await res.json();
```

</details>

<details>
  <summary><b>List users</b></summary>

Endpoint: `GET /user`

Code example:

```javascript
const res = await fetch(
  "https://67c888390acf98d07086f189.mockapi.io/api/v1/user",
  {
    method: "GET",
    headers: { "content-type": "application/json" }
  }
);
const users = await res.json();
```

</details>

<details>
  <summary><b>Retrieve a single user</b></summary>

Endpoint: `GET /user/:userId`

Code example:

```javascript
const res = await fetch(
  "https://67c888390acf98d07086f189.mockapi.io/api/v1/user/1",
  {
    method: "GET",
    headers: { "content-type": "application/json" }
  }
);
const user = await res.json();
```

</details>

<details>
  <summary><b>List events</b></summary>
  
Endpoint: `GET /event`

Code example:

```javascript
const res = await fetch(
  "https://67c888390acf98d07086f189.mockapi.io/api/v1/event",
  {
    method: "GET",
    headers: { "content-type": "application/json" },
  }
);
const events = await res.json();
```

</details>

<details>
  <summary><b>Retrieve a single event</b></summary>
  
Endpoint: `GET /event/:eventId`

Code example:

```javascript
const res = await fetch(
  "https://67c888390acf98d07086f189.mockapi.io/api/v1/event/1",
  {
    method: "GET",
    headers: { "content-type": "application/json" },
  }
);
const event = await res.json();
```

</details>

<details>
  <summary><b>Attend an event</b></summary>

Endpoint: `POST /event/:eventId/attendance`

Code example:

```javascript
const res = await fetch(
  "https://67c888390acf98d07086f189.mockapi.io/api/v1/event/1/attendance",
  {
    method: "POST",
    headers: { "content-type": "application/json" },
    body: JSON.stringify({
      status: "CONFIRMED",
      userId: "6",
    }),
  }
);
const attendance = await res.json();
```

</details>

<details>
  <summary><b>Update attendance status</b></summary>

Endpoint: `PATCH /event/:eventId/attendance/:attendanceId`

Code example:

```javascript
const res = await fetch(
  "https://67c888390acf98d07086f189.mockapi.io/api/v1/event/1/attendance/19",
  {
    method: "PATCH",
    headers: { "content-type": "application/json" },
    body: JSON.stringify({
      status: "MAYBE",
    }),
  }
);
const event = await res.json();
```

</details>

#### Additional doc

- Filtering: https://github.com/mockapi-io/docs/wiki/Code-examples#filtering
- Pagination: https://github.com/mockapi-io/docs/wiki/Code-examples#pagination
- Sorting: https://github.com/mockapi-io/docs/wiki/Code-examples#sorting

## What we are evaluating 🔍

- **Understanding requirements & problem solving:**  
  Assess your ability to comprehend the requirements and design an effective interface.
- **Communication:**  
  Clearly articulate any doubts and explain your design decisions.
- **Adaptability to our stack:**  
  We value proficiency in React and adherence to frontend best practices.
- **UI/UX Design & Best Practices:**  
  Focus on modularity, testability, performance, and overall user experience.
- **Development principles:**  
  Consider the following:
  - **Idempotency:** The UI should behave consistently with valid inputs. 🔄
  - **Testability:** Provide tests to ensure your components work as expected. ✅
  - **Performance & Scalability:** Ensure your interface is efficient and responsive even with multiple interactions. ⚡

## Additional considerations 📌

- **Documentation:**  
  Provide clear documentation on your design and instructions for running your code.
- **Inline comments:**  
  Include inline comments to explain key or complex decisions.
- **Commits:**  
  Make frequent, descriptive commits that reflect your development process.

## Instructions 🔧

Two options to submit the test:

### GitHub

1. [Fork](https://github.com/wuolah/test-frontend-developer/fork) this repository.
2. Create a branch with your name.
3. Once complete, create a [Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) for review.

### Email

Via email to juanlu@wuolah.com

If you have any questions, please open an issue in the repository or contact **juanlu@wuolah.com**.

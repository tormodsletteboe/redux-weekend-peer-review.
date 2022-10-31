# Weekend Challenge 11 - React-Redux Feedback Form

## Instructions

Reviewing code is an important role developers play. We're going to practice reviewing code from others.

- Get the repo url from your partner
- Get your partner's project running on your computer
- Review the code from your partner and give relevant feedback
- Complete the Markdown section and submit that in the notes section on the assignment app. (Make sure you include who's code you reviewed.)

Practicing compassionate code reviews is important (you can learn more from this video on the topic: https://www.youtube.com/watch?v=Ea8EiIPZvh0 )

## Review Checklist

## Base Required Features 

- Multi-Part Form:  
  - [X] Able to add feedback
    - [X] Data collected on individual pages & components
    - [X] Click on next takes you to the next page in sequence
    - [X] Data saves in DB after *all* the parts are completed (not piecemeal)
    - [X] Thank you page takes you back to the first view
    - [X] Old Data is cleared on form completion

- Client code:
  - [X]  Individual components for each form part
  - [X]  Redux setup complete
    - [X] Store linked to react with `<Provider>`
    - [X] Store setup with reducer(s) and logger middleware 
  - [X] Reducers & Actions Working
    - [X] Actions are in SCREAMING_SNAKE_CASE and semantically named
    - [X] Actions have a `type` key, and `payload` if sending data
          - not sure i understand the flagged reducer
    - [X] Reducers are returning a new state, or the old state (not mutating)
    - [NA] Reducers are using spread correctly (to keep old data, while adding new)
  - [x] Review Component shows at all times with current redux state
  - [x] React-Redux Working
    - [x] Dispatching actions onClick
    - [x] Grabbing data from the redux store with `useSelector`
  - [x] Axios POST request to add feedback


- Server code:   
  - [x] Router made for GET, POST


## General Items
Feedback should be provided for these items, but they do not impact scoring.

- Git 
  - [X] Multiple git commits showing incremental progress
  - [x] Commits are descriptive of the changes made or feature added 
  - [X] Has .gitignore with node_modules
  - [X] Readme file updated (assuming this is previously discussed)
- Code Style 
  - [X] Appropriate amount of code comments
  - [X] Code is consistently formatted
- Client
  - [X] Appropriate use of HTML tags
  - [X] Basic CSS styling with margins/padding


## Stretch Goals
First must be complete for score of  _Exceeds Expectations_

- Previous Steps
  - [X] allows a user to go to a previous step, either directly or by cycling backward thru the steps
  - [x] user can upate their score for a step
    - [x] new score is validated to not be empty
    - [x] redux is updated with new score
  - [x] user can continue on to review page and submit as in Base Mode


- Admin View
  - [x] All entries are visible with correct data from inputs
    - [x] Most recent is at the top
  - [x] Can Delete an entry
    - [x] User is prompted before deleting
  - [x] Axios GET request to get all feedback for `/admin` view in componentDidMount

  Busywork Goals, consider removing or making more useful

- [ ] Styling with Material UI
- [x] Ability to flag a feedback item on `/admin` for further review
- [ ] Deployed to Heroku


## Markdown

```
Hey __Chris Maki_,

General Feedback. provided by Tormod Sletteboe

Great work, everything works fine. Awesome job on commenting and CSS, easy to read code as well. Only thing I could pick at is your fetch call 
in you App.jsx is not needed. You call fetch after posting, but the fetch is not really doing anything.
Also maybe use useEffect and call the redux store to show what the previous selection was, ie, when user goes back 1 page,
the input does not display what they previously chose.
And there seems to be an server error on delete in the admin page, but it does delete though so not sure.


---
| Functional Requirements | Complete? | YES
| --- | :---: |
| Multi page form with client side routing and navigation (next button) | YES |
| Data stored in Redux when navigating from page to page | YES |
| User is notified when trying to leave a blank score | YES |
| Review Component displays scores and comments from current redux state | YES |
| Submit button sends data to the server via Axios | YES |
| Confirmaion Page displays after data is POSTed to the server | YES |
| Button on Confirmation Page clears Redux and starts a new survey | YES |
| Views are broken down into components | YES |

---
### Notes:

Notes on the above Functional Requirements.
I like your window.location.reload(); in your review.jsx file, nifty

---
| General Items | Complete? |
| --- | :---: |
| More than 15 git commits | YES |
| Commits are descriptive of the changes made or feature added | YES mostly |
| Readme file updated | YES |
| Appropriate amount of code comments | YES |
| Code is consistently formatted | YES |
| Server code organized with router & module files | YES |

---
### Notes:

Notes on General Items
Great job

```

# Livongo FE Coding Challenge
Complete the two stories below to finalize a fictitious Livongo blood sugar reading logging.

## Prerequisites
* `node/npm`

## Use Story 1
Users should be able to filter blood sugar readings by meal tags.

### Requirements
Add a modal with a checkbox list of meal tags, allow the user to select specific tags and filter the list of blood sugar readings after clicking the button **Save**. Follow [the design](/screens/filter-by-meal-modal.png) provided by the product team.

- [ ] The modal should animate in and out gracefully, not just appear/disappear.
- [ ] The modal should be responsive and take the whole screen in a mobile device screen size.

![New Blood Sugar Modal](/screens/filter-by-meal-modal.png)

![New Blood Sugar Modal](/screens/filter-by-meal-modal-mobile.png)

## User Story 2
Users want to manually add a blood sugar reading to their logs.

### Requirements
Implement a modal where an user can manually add a new blood sugar reading. Follow [the design](/screens/new-blood-sugar-modal.png) provided by the product team.

- [ ] You may use any calendar widget you want for the field **Date**.
- [ ] The fields **Date** and **Time** should default to the current date and time.
- [ ] The field **Blood Sugar Value** a) is required, b) should only allow numbers, c) be maximum 999, and d) should [display an error](/screens/new-blood-sugar-modal-error.png) if not filled out correctly.
- [ ] The new blood sugar reading should be sent to the API and added to the UI in the correct order based on the date and time.
- [ ] Make sure that a second reading can be added and the UI updates correctly.

![New Blood Sugar Modal](/screens/new-blood-sugar-modal.png)

## Directions
You may use any additional open source tools you wish to satisfy the requirements.

1. Fork this repository to your own GitHub account.
1. Run `npm install` to download all necessary dependencies.
1. Run `npm start` to serve the API *(see API notes below)* and spin up the local development environment.
1. Implement your solution.
1. Download your fork as a zip file and upload it to the relevant location within [Greenhouse](http://greenhouse.io).

## API
The API lives at `http://localhost:8001/api`.

Available routes include:
* `GET /blood-sugar-readings` - Get a list of blood sugar readings.
* `POST /blood-sugar-readings` - Save a new blood sugar reading.
    ```
    {
        id: int,
        value: int,
        date: string (MM-DD-YYYY),
        time: string (hh:mm:ss-Z),
        mealTag: string,
        note: string
    }
    ```

## Notes
* Would anything here make sense to unit/integration test?
* Remember, the devil is in the details :)

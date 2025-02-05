# Kantox Frontend Engineer Tech Test  

## Overview  

The goal of this test is to evaluate how you analyze and solve problems, structure your code, and approach UX/UI design. You have the freedom to use any JavaScript framework, tools, or libraries you prefer.  

## Task Description  

You will be provided with an empty NPM project along with a `data.json` file containing order information retrieved from a JSON API. Your task is to build a simple frontend application that includes:  

### 1. **Home Page**  
- This page should provide an overview of your implementation.  
- Briefly describe the technologies you used and the approach you took to solve the exercise.  

### 2. **Orders Page**  
- Display the order data from `data.json` in a structured table.  
- The table should include the following key attributes:  

  - **Reference:** Unique identifier for the order.  
  - **Order Type:** Type of order (e.g., `forward`, `swap`, `ndf`).  
  - **Creation Date:** The date the order was created.  
  - **Market Direction:** Indicates whether the order is a `buy` or `sell`.  
  - **Buy / Sell Columns:**  
    - If `market-direction` is `"buy"`, display the amount (converted from `amount-cents`) and `buy-currency` in the **Buy** column. The **Sell** column should display only the `sell-currency`.  
    - If `market-direction` is `"sell"`, display the amount (converted from `amount-cents`) and `sell-currency` in the **Sell** column. The **Buy** column should display only the `buy-currency`.  
    - **Conversion Rule:** The value in `amount-cents` should be converted to a monetary format, assuming the last two digits represent cents. For example, `10000` should be displayed as `100.00`.  
  - **Value Date:** The execution date of the order.  
  - **Status:** Current status of the order (`new`, `failed`, `awaiting_response`, etc.).  
  - **Actions: (Optional Task):** Possible actions for the order (`edit`, `delete`, `execute`, `retry`, etc.) as an inline/dropdown menu 
  - **Bank Name (Optional Task):** Display the associated bank name.  

### 3. **Optional Task - Bank Account Details**  
- Each order has a relationship with a bank account under the `relationships` field.  
- If implemented, the table should display the bank name, and clicking on it should open a modal or popup with more details, including:  
  - **Bank Name**  
  - **Account Number**  
  - **SWIFT Code**  
  - **Address**  
  - **Phone**  
  - **Email**  

## Additional Notes  

- You can use any JavaScript framework (Ember, Svelte, React, Vue, etc.) or vanilla JavaScript.
- You can crate your own CSS, use a CSS framework (Tailwind, etc.) or any Components library (Flowbite, Material UI, etc.)
- The UI/UX quality will be evaluated, so pay attention to usability and accessibility.  
- Keep the code well-structured and easy to read.  
- Feel free to add any additional enhancements you believe improve the project.  

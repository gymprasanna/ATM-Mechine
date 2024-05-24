pin_codes = [1234, 4321]  # List of PIN codes
atm_card = 'Inserted your card successfully - ' 
print(atm_card)

attempts = 0  # Counter for incorrect attempts

while attempts < 3:  # Allow up to 3 attempts
    pin = int(input('Enter your PIN: '))

    if pin in pin_codes:  # Check if the entered PIN is in the list of PIN codes
        print('Your PIN is correct')
        money = int(input('How much money are you withdrawing?: '))
        temp = 0
        while temp < money:  # Keep counting money until it exceeds the entered amount
            temp += 100
            if temp <= money:
                print('Count:', temp, 'Total Money:', money)
            else:
                print('Total Money:', money)
        break  # Exit the loop if the correct PIN is entered
    else:
        attempts += 1  # Increment the attempt counter
        print('Your PIN is wrong. Attempts remaining:', 3 - attempts)

if attempts == 3:
    print('Maximum number of attempts reached. Your card is blocked.')

    
    
    
    

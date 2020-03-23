# Code-Quiz

# Project Title
Week 4 Homework Project - Code Quiz

# Motivation 
This homework file will deliver a quiz game that is cutomizable to deliver new content with minor edits to the java code. It can be expanded to accept many categories and an unlimited number of questions per category with dyanmic time applied based on the number of questions and individual scores saved for each category.

# Code Style
This project is written using Java script and the Bootstrap CDN for layout and mobile responsiveness. Bootstrap Java libraries are included but not ulilized.

# Screenshots
![instructions](assets/instructions.JPG "Instructions Screen")



# Features
Character limit prompt will not only reject numbers outside of the accepted range but will also reject string input and round decimals down.

Character set is built based on user selection to ensure that results match desired outcome.

After the password is generated, it is checked to make sure it contains at least one of each desired character set. This allows a truly random selection while also ensuring the password matches user specficiations.

# Code Example
This while loop rejects inputs that don't meet the minimum standards until valid selection is made

    while(uPassword != true && lPassword != true && nPassword != true && sPassword != true) {
        var uPassword = confirm ("Would you like to include upper case characters?");
        var lPassword = confirm ("Would you like to include lower case characters?");
        var nPassword = confirm ("Would you like to include numerical characters?");
        var sPassword = confirm ("Would you like to include special characters?");
        if (uPassword != true && lPassword != true && nPassword != true && sPassword != true) {
        alert("Your password must contain at least ONE character set selection");
        }
    }


  This section is responsible for checking each character in the generated password to verify whether it was found in the separate character array.

    for (i=0;i<numPassword;i++) {
        // Loops once through each character in character array
        for(n=0;n<uChars.length;n++) {
            if (tempPassword[i] == uChars[n]) {
            var uFound = true;
            }
        }
        for(n=0;n<lChars.length;n++) {
            if (tempPassword[i] == lChars[n]) {
            var lFound = true;
            }
        }
        for(n=0;n<nChars.length;n++) {
            if (tempPassword[i] == nChars[n]) {
            var nFound = true;
            }
        }
        for(n=0;n<sChars.length;n++) {
            if (tempPassword[i] == sChars[n]) {
            var sFound = true;
            }
        }
        }

# How to Use
Click "Generate Password" to begin the password generation process. Follow the prompts to make selections. Click "cancel" on the first prompt to exit the loop.


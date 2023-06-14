
# Anti Bypasser Library

The Anti Bypasser library is a tool that prevents any kinds of hooks, bypassers, sniffers (i.e httpdebugger, fiddler, etc) and allows for secure connection (using secure_connection method in the library).

This also prevents reversers from bypassing your authentication, for example:

KeyAuth\
Auth.GG

KeyAuth and Auth.GG users can use this to prevent any kind of bypassing of their authentication.
## Installation

To use the Anti Bypasser library, simply purchase it on the website: https://bitservices.mysellix.io/product/647cf2cb543ef

## Usage

To initialize the library, create a new instance of the AntiBypasser class with your API key:

```csharp
var antiBypasser = new AntiBypasser("key");
```

### Preventing Bypassers

To prevent bypassers, use the DetectPatches method:

```csharp
if (antiBypasser.DetectPatches(typeof(Program).Assembly))
{
    Console.ForegroundColor = ConsoleColor.Red;
    Console.WriteLine("Bypass detected!");
    Console.ReadKey();
    return;
}
```

### Preventing Sniffers

To prevent sniffers, create a new instance of the SnifferDetection class and use the DetectSniffer method:

```csharp
if (antiBypass.CheckSniffer())
{
    Console.ForegroundColor = ConsoleColor.Red;
    Console.WriteLine("Sniffer detected!");
    Console.ReadKey();
    return;
}
```

### Using Secure Connection

To use secure connection, create a new instance of the SecureConnection class and set the necessary certificates:

```csharp
List<string> yourCertificates = new List<string>
{
    "DigiCert TLS"
};
bool isSuccess = antiBypass.SecureConnection(() => Task.Run(async () =>
{
    //Your code here to securely download or upload something.
 
}), yourCertificates);

if (isSuccess) //Note that it automatically does not execute the code if it doesn't succeed.
{
    Console.ForegroundColor = ConsoleColor.Green;
    Console.WriteLine("Secure connection success.");
    Console.ReadKey();
    return;
}
```

## Discord Server

https://discord.gg/skrkgergAM

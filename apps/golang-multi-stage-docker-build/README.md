# Multi Stage Docker Build

The main purpose of choosing a golang based applciation to demostrate this example is golang is a statically-typed programming language that does not require a runtime in the traditional sense. Unlike dynamically-typed languages like Python, Ruby, and JavaScript, which rely on a runtime environment to execute their code, Go compiles directly to machine code, which can then be executed directly by the operating system.

So the real advantage of multi stage docker build and distro less images can be understand with a drastic decrease in the Image size.

## Distroless image 
- Distroless images are a type of container image that excludes the majority of a Linux distribution's codebase, resulting in a smaller, more streamlined image. 
- They are created by removing unnecessary packages and files, making them ideal for applications that require a minimal footprint. 
- This approach reduces the attack surface and improves security, as fewer dependencies means fewer potential vulnerabilities. 
- Distroless images are commonly used in cloud-native applications, serverless functions, and other use cases where size and security are critical considerations. 

## Redhat Universal Base Image
- Universal Base Image Micro (UBI Micro) is a stripped down image that uses the package manager on the underlying host to install packages, typically using Buildah, or Multi-stage builds with Podman
- Ubi-micro has the minimal size but it doesn't come with any installed package manager like yum/dnf. 
- Ubi-minimal has more than ubi-micro but it comes with microdnf package manager installed Ubi or Ubi Standard has both yum and dnf package installed.
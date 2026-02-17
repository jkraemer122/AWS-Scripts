# AWS Scripts

A collection of AWS automation scripts I've built while working through real problems over 5+ years in cloud support. These tackle common headaches in IAM management, security compliance, resource automation, and day-to-day AWS operations.

## What's Here

This repo has proof-of-concept scripts for problems I kept running into with enterprise AWS environments. They work and they're tested in dev environments, but treat them as starting points, not production-ready solutions you can just drop in.

I wrote these to be readable and educational. If you're learning AWS or debugging something, you shouldn't have to spend 20 minutes figuring out what a script actually does.

## Repository Structure

```
aws-scripts/
├── iam/              # Identity and Access Management utilities
├── config/           # AWS Config automation and compliance tools
├── s3/               # S3 bucket management and operations
├── lambda/           # Lambda function utilities and helpers
└── cloudformation/   # CloudFormation template generators and validators
```

Each directory contains its own README with specific script documentation, usage examples, and any relevant prerequisites.

## Prerequisites

- AWS CLI configured with appropriate credentials
- Python 3.8+
- Boto3 library
- IAM permissions for whatever services you're working with

Individual scripts might need extra stuff - check their directories for specifics.

## Usage Philosophy

**Readable over clever** - I went for code you can actually understand instead of trying to be slick with one-liners. Debugging at 2am is hard enough without having to decipher what past-me was thinking.

**Fail safely** - These include validation and dry-run options where it makes sense. Nobody wants to be the person who broke prod.

**Actual problems** - Every script here exists because I ran into the same annoying task or complex issue enough times that automation became worth it.

## Common Use Cases

**IAM Management**
- Auditing permissions across accounts
- Identifying overly permissive policies
- Generating least-privilege policy recommendations

**Config Compliance**
- Automated compliance checks
- Custom Config rule deployments
- Remediation automation for common violations

**S3 Operations**
- Bulk bucket policy updates
- Lifecycle policy management
- Access logging configuration

**Lambda Utilities**
- Function deployment helpers
- Log analysis tools
- Performance monitoring scripts

**CloudFormation**
- Template validation and linting
- Stack drift detection
- Resource dependency mapping

## Security Note

These scripts focus on security and compliance, but they're still proof-of-concept. Before you use them in production:

- Actually read the code
- Test in a sandbox environment first
- Make sure you understand what IAM permissions they need
- Check if they fit your org's security policies
- Add error handling for your specific setup

Basically, don't just yolo these into production.

## Contributing

Pull requests are welcome. This is mostly a portfolio project, but if you've improved something or adapted a script for a related problem, I'm happy to look at it.

For bigger changes, open an issue first so we can talk through it.

## Background

I'm a Cloud Support Engineer who's spent a lot of time in AWS security services, especially IAM and Config. These scripts come from working on everything from one-off support cases to full enterprise security overhauls. They're solutions to problems I kept seeing over and over.

## License

MIT License - use however you want. Attribution is nice but not required.

## Disclaimer

These scripts are provided as-is, without warranty. They're educational tools and proof-of-concept solutions. Test thoroughly before using in production environments, and always follow AWS best practices for your specific use case.

---

**Questions? Issues?** Open an issue on this repository. I'm generally responsive to genuine questions, though I can't provide production support for these scripts.

# Release Information 

- **Version**: 1.0.0 
- **Certified**: No 
- **Publisher**: Fortinet 
- **Compatible Version**: FortiSOAR 7.4.0 and later 

# Overview 

Successful exploitation could allow attackers to execute arbitrary code within the PHP application process, potentially compromising the affected server and exposing sensitive data, application files, or connected databases, depending on the process privileges and system configuration.

FortiGuard Labs is monitoring the PHP2Shell vulnerabilities and related threat activity. Updates will be provided as new threat intelligence emerges and additional protections become available. Organizations are advised to apply the relevant security updates and consult the FortiGuard coverage information for the latest protection status. 

 The **Outbreak Response - PHP2Shell Remote Code Execution Vulnerabilities** solution pack works with the Threat Hunt rules in [Outbreak Response Framework](https://github.com/fortinet-fortisoar/solution-pack-outbreak-response-framework/blob/release/2.3.0/docs/background-information.md#threat-hunt-rules) solution pack to conduct hunts that identify and help investigate potential Indicators of Compromise (IOCs) associated with this vulnerability within operational environments of *FortiSIEM*, *FortiAnalyzer*.

 The [FortiGuard Outbreak Page](https://www.fortiguard.com/outbreak-alert/php2shell) contains information about the outbreak alert **Outbreak Response - PHP2Shell Remote Code Execution Vulnerabilities**. 

## Background: 

PHP is an open-source, server-side scripting language widely used to build dynamic websites and web applications. It powers content management systems, e-commerce platforms, and other web services, including WordPress, which relies on PHP to run its core functionality. According to W3Techs, as of October 21, 2026, PHP was used by 69.3% of websites whose server-side programming language is known. 

Because PHP is deployed across a large portion of the web, vulnerabilities in its underlying runtime can affect many different applications and hosting environments. The PHP2Shell vulnerabilities are particularly serious because successful exploitation could allow unauthenticated attackers to execute arbitrary code on vulnerable servers, potentially exposing sensitive data and enabling further compromise. The broad use of PHP makes timely patching and identifying vulnerable deployments especially important.

CVE-2026-109618 - RCE via out-of-memory corruption: An out-of-memory condition can interrupt PHP while internal request data is only partially initialized. Subsequent request-cleanup operations may incorrectly process this invalid data, potentially enabling remote code execution.

CVE-2026-109619 - RCE via stale global state: Internal request state can persist after its associated memory has been freed. A later request handled by the same worker may access this stale state before normal initialization resets it, potentially enabling remote code execution.

PHP announced emergency security updates for October 21, 2026, following reports that details of the vulnerabilities had leaked ahead of the planned disclosure. Subsequent reports highlighted ongoing exploit research and potential attack activity, underscoring the urgency of applying the available patches. However, widespread exploitation of either vulnerability has not been independently confirmed. 

## Announced: 

FortiGuard Labs recommends a defense-in-depth approach to reduce exposure to attacks targeting vulnerable PHP deployments and is currently monitoring the situation and will provide updates as new information becomes available and additional protections are released. Organizations should prioritize patching internet-facing PHP servers and other exposed deployments immediately. Apply the security updates. Upgrade to PHP 8.5.12, 8.4.27, 8.3.36, or 8.2.35, as appropriate. Organizations using vendor-maintained packages should apply the corresponding security updates from their distributions or service providers. 

## Latest Developments: 

October 21, 2026: PHP published details of both critical remote code execution vulnerabilities and released security updates for PHP 8.5.12, 8.4.27, 8.3.36, and 8.2.35. Government cybersecurity agencies also issued advisories urging organizations to patch.
https://www.php.net/archive/2026.php#2026-10-20-1

October 21, 2026: Additional threat intelligence reporting detailed exploitation attempts, public proof-of-concept research, and mitigation guidance. Organizations were advised to prioritize patching internet-facing PHP deployments.
https://www.fortiguard.com/threat-signal-report/6551/php2shell-remote-code-execution-vulnerabilities

October 20, 2026: Details of CVE-2026-109618 and CVE-2026-109619 circulated publicly ahead of the planned disclosure, prompting PHP to advance its security release.

October 17, 2026: Amazon Threat Intelligence identified an exploitation attempt targeting PHP2Shell in its MadPot telemetry, dated four days before public disclosure.
https://aws.amazon.com/blogs/security/amazon-threat-intelligence-identifies-php2shell-exploitation-prior-to-public-disclosure-in-madpot

August 1, 2026: Calif identified a vulnerability through AI-assisted source-code analysis and later reported the first flaw to the PHP project.
https://calif.io/php2shell/ 

# Next Steps
 | [Installation](./docs/setup.md#installation) | [Configuration](./docs/setup.md#configuration) | [Usage](./docs/usage.md) | [Contents](./docs/contents.md) | 
 |--------------------------------------------|----------------------------------------------|------------------------|------------------------------|
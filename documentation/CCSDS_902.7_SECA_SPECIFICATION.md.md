\# CCSDS 902.7-M-1 & IOAG Service Catalog \#1 (SECA) Specification

\#\# Executive Summary  
This document provides the technical specification and architecture for \*\*SECAForge Pro\*\*, an industrial aerospace workstation implementing the \*\*Consultative Committee for Space Data Systems (CCSDS) 902.7-M-1\*\* Recommended Practice (\*Cross Support Service Management—Service Catalog\*, Magenta Book) and the \*\*Interagency Operations Advisory Group (IOAG) Service Catalog \#1\*\*.

In international space communications, before missions can negotiate Service Agreements (SACP) or schedule tracking passes (SSF/SPDF), space agencies (NASA, ESA, JAXA, ISRO, MBRSC) and commercial network providers publish standardized, machine-readable \*\*Service Catalogs (SECA)\*\*. These catalogs formally publish aperture assets, geodetic locations, supported frequency bands (S/X/Ka/Optical), RF transmitter power envelopes, receiver G/T sensitivities, radiometric tracking capabilities, and underlying protocol interface bindings (SLE, CSTS, CFDP).

\#\# 1\. CSS-SM Service Lifecycle Architectural Context  
0\. Service Catalog (SECA): CCSDS 902.7-M-1 & IOAG \#1 \[\#488\]  
1\. Service Agreement & Profiles: CCSDS 902.5-B-1 (SACP) \[\#486\]  
2\. Communications Planning: CCSDS 902.2-B-1 (CPIF) \[\#482\]  
3\. Service Utilization Request: CCSDS 902.9-B-1 (SMURF) \[\#485\]  
4\. Simple Schedule Agreement: CCSDS 902.1-B-1 (SSF) \[\#481\]  
5\. Service Package Provisioning: CCSDS 902.4-B-1 (SPDF) \[\#483\]  
6\. Event Sequence Execution: CCSDS 902.6-B-1 (EVSQ) \[\#484\]  
7\. Service Accounting: CCSDS 902.8-B-1 (SMAC) \[\#487\]

\#\# 2\. Service Catalog (SECA) Data Entity Model  
\- Header: catalogId, providerCsss, publicationTime, standardReference, version.  
\- Service Definitions (IOAG Service Catalog \#1): Forward CLTU, Return RAF/RCF, Radiometric Doppler/Ranging/Delta-DOR, CFDP File Delivery.  
\- Aperture Registry: apertureId, geodetic coordinates, dish diameter (\>=34m), G/T figure of merit, max transmitter power, supported spectrum bands.  
\- Capability Query Engine: real-time matching of mission communications link budgets against aperture catalog assets.  

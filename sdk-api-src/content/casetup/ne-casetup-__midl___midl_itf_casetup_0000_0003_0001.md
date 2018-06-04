---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __MIDL___MIDL_itf_casetup_0000_0003_0001 enumeration


## -description


The <b>MSCEPSetupProperty</b> enumeration specifies a property type for setup and configuration of a Microsoft <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Simple Certificate Enrollment Protocol</a> (SCEP) role using <a href="https://msdn.microsoft.com/328c6c04-7ade-4b64-bd8a-4314b6e8dc78">IMSCEPSetup</a>.


## -enum-fields




### -field ENUM_CEPSETUPPROP_USELOCALSYSTEM

A <b>VT_BOOL</b> value that specifies whether the Microsoft SCEP ISAPI Extension runs as the  local system user or under a separate user account. For remote CA or standalone CA configurations, by default this is set to <b>VARIANT_FALSE</b>. For a local enterprise CA configuration, by default this is set to <b>VARIANT_TRUE</b>.


### -field ENUM_CEPSETUPPROP_USECHALLENGE

A <b>VT_BOOL</b> value that specifies whether to require an SCEP challenge phrase to enroll. By default, setup sets this to <b>TRUE</b>.


### -field ENUM_CEPSETUPPROP_RANAME_CN

A <b>VT_BSTR</b> value that specifies the common name for Microsoft SCEP registration authority (RA) certificate name information. By default, the common name format is <i>MachineName</i>"-RA", where <i>MachineName</i> is the local machine name.


### -field ENUM_CEPSETUPPROP_RANAME_EMAIL

A <b>VT_BSTR</b> value that specifies an optional email address to be added in Microsoft SCEP RA certificate name information.


### -field ENUM_CEPSETUPPROP_RANAME_COMPANY

A <b>VT_BSTR</b> value that specifies an optional company name to be added in Microsoft SCEP RA certificate name information.


### -field ENUM_CEPSETUPPROP_RANAME_DEPT

A <b>VT_BSTR</b> value that specifies an optional department name to be added in Microsoft SCEP RA certificate name information.


### -field ENUM_CEPSETUPPROP_RANAME_CITY

A <b>VT_BSTR</b> value that specifies an optional city name to be added in Microsoft SCEP RA certificate name information.


### -field ENUM_CEPSETUPPROP_RANAME_STATE

A <b>VT_BSTR</b> value that specifies an optional state name to be added in Microsoft SCEP RA certificate name information.


### -field ENUM_CEPSETUPPROP_RANAME_COUNTRY

A <b>VT_BSTR</b> value that specifies the country or region name to be added in Microsoft SCEP RA certificate name information. By default, setup uses the country or region setting for the local computer.


### -field ENUM_CEPSETUPPROP_SIGNINGKEYINFORMATION

A <b>VT_IDISPATCH</b> value that is made up of an <a href="https://msdn.microsoft.com/d27c9ba5-ddee-4c9c-b812-e61b974b515a">ICertSrvSetupKeyInformation</a> object used to create a Microsoft SCEP signing certificate. Setup creates a signing certificate based on an "EnrollmentAgentOffline" template.


### -field ENUM_CEPSETUPPROP_EXCHANGEKEYINFORMATION

A <b>VT_IDISPATCH</b> value that is made up of an <a href="https://msdn.microsoft.com/d27c9ba5-ddee-4c9c-b812-e61b974b515a">ICertSrvSetupKeyInformation</a> object used to create a Microsoft SCEP key exchange certificate. Setup creates a key exchange certificate based on a "CEPEncryption" template.


### -field ENUM_CEPSETUPPROP_CAINFORMATION

A <b>VT_BSTR</b> value that specifies the Certification Authority (CA) information. By default, setup uses the local CA. If a local CA is present,  you should not set this property.


### -field ENUM_CEPSETUPPROP_MSCEPURL

A <b>VT_BSTR</b> value that specifies the URL for use by routers to connect and send certificate requests using SCEP. By default, setup uses http://<i>MachineName</i>/certsrv/mscep/mscep.dll, where <i>MachineName</i> is the local machine name. This is a read-only property.


### -field ENUM_CEPSETUPPROP_CHALLENGEURL

A <b>VT_BSTR</b> value that specifies the URL for use by router administrators to connect and obtain a challenge phrase. By default, setup uses http://<i>MachineName</i>/certsrv/mscep/, where <i>MachineName</i> is the local machine name. This is a read-only property.


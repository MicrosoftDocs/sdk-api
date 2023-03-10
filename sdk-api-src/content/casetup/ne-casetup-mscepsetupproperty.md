---
UID: NE:casetup.__MIDL___MIDL_itf_casetup_0000_0003_0001
title: MSCEPSetupProperty (casetup.h)
description: Specifies a property type for setup and configuration of a Microsoft Simple Certificate Enrollment Protocol (SCEP) role using IMSCEPSetup.
helpviewer_keywords: ["ENUM_CEPSETUPPROP_CAINFORMATION","ENUM_CEPSETUPPROP_CHALLENGEURL","ENUM_CEPSETUPPROP_EXCHANGEKEYINFORMATION","ENUM_CEPSETUPPROP_MSCEPURL","ENUM_CEPSETUPPROP_RANAME_CITY","ENUM_CEPSETUPPROP_RANAME_CN","ENUM_CEPSETUPPROP_RANAME_COMPANY","ENUM_CEPSETUPPROP_RANAME_COUNTRY","ENUM_CEPSETUPPROP_RANAME_DEPT","ENUM_CEPSETUPPROP_RANAME_EMAIL","ENUM_CEPSETUPPROP_RANAME_STATE","ENUM_CEPSETUPPROP_SIGNINGKEYINFORMATION","ENUM_CEPSETUPPROP_USECHALLENGE","ENUM_CEPSETUPPROP_USELOCALSYSTEM","MSCEPSetupProperty","MSCEPSetupProperty enumeration [Security]","casetup/ENUM_CEPSETUPPROP_CAINFORMATION","casetup/ENUM_CEPSETUPPROP_CHALLENGEURL","casetup/ENUM_CEPSETUPPROP_EXCHANGEKEYINFORMATION","casetup/ENUM_CEPSETUPPROP_MSCEPURL","casetup/ENUM_CEPSETUPPROP_RANAME_CITY","casetup/ENUM_CEPSETUPPROP_RANAME_CN","casetup/ENUM_CEPSETUPPROP_RANAME_COMPANY","casetup/ENUM_CEPSETUPPROP_RANAME_COUNTRY","casetup/ENUM_CEPSETUPPROP_RANAME_DEPT","casetup/ENUM_CEPSETUPPROP_RANAME_EMAIL","casetup/ENUM_CEPSETUPPROP_RANAME_STATE","casetup/ENUM_CEPSETUPPROP_SIGNINGKEYINFORMATION","casetup/ENUM_CEPSETUPPROP_USECHALLENGE","casetup/ENUM_CEPSETUPPROP_USELOCALSYSTEM","casetup/MSCEPSetupProperty","security.mscepsetupproperty"]
old-location: security\mscepsetupproperty.htm
tech.root: security
ms.assetid: c3740afc-842e-427f-87bf-022f5544d0d4
ms.date: 12/05/2018
ms.keywords: ENUM_CEPSETUPPROP_CAINFORMATION, ENUM_CEPSETUPPROP_CHALLENGEURL, ENUM_CEPSETUPPROP_EXCHANGEKEYINFORMATION, ENUM_CEPSETUPPROP_MSCEPURL, ENUM_CEPSETUPPROP_RANAME_CITY, ENUM_CEPSETUPPROP_RANAME_CN, ENUM_CEPSETUPPROP_RANAME_COMPANY, ENUM_CEPSETUPPROP_RANAME_COUNTRY, ENUM_CEPSETUPPROP_RANAME_DEPT, ENUM_CEPSETUPPROP_RANAME_EMAIL, ENUM_CEPSETUPPROP_RANAME_STATE, ENUM_CEPSETUPPROP_SIGNINGKEYINFORMATION, ENUM_CEPSETUPPROP_USECHALLENGE, ENUM_CEPSETUPPROP_USELOCALSYSTEM, MSCEPSetupProperty, MSCEPSetupProperty enumeration [Security], casetup/ENUM_CEPSETUPPROP_CAINFORMATION, casetup/ENUM_CEPSETUPPROP_CHALLENGEURL, casetup/ENUM_CEPSETUPPROP_EXCHANGEKEYINFORMATION, casetup/ENUM_CEPSETUPPROP_MSCEPURL, casetup/ENUM_CEPSETUPPROP_RANAME_CITY, casetup/ENUM_CEPSETUPPROP_RANAME_CN, casetup/ENUM_CEPSETUPPROP_RANAME_COMPANY, casetup/ENUM_CEPSETUPPROP_RANAME_COUNTRY, casetup/ENUM_CEPSETUPPROP_RANAME_DEPT, casetup/ENUM_CEPSETUPPROP_RANAME_EMAIL, casetup/ENUM_CEPSETUPPROP_RANAME_STATE, casetup/ENUM_CEPSETUPPROP_SIGNINGKEYINFORMATION, casetup/ENUM_CEPSETUPPROP_USECHALLENGE, casetup/ENUM_CEPSETUPPROP_USELOCALSYSTEM, casetup/MSCEPSetupProperty, security.mscepsetupproperty
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MSCEPSetupProperty
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_casetup_0000_0003_0001
 - casetup/__MIDL___MIDL_itf_casetup_0000_0003_0001
 - MSCEPSetupProperty
 - casetup/MSCEPSetupProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Casetup.h
api_name:
 - MSCEPSetupProperty
---

# MSCEPSetupProperty enumeration


## -description

The <b>MSCEPSetupProperty</b> enumeration specifies a property type for setup and configuration of a Microsoft <a href="/windows/desktop/SecGloss/s-gly">Simple Certificate Enrollment Protocol</a> (SCEP) role using <a href="/windows/desktop/api/casetup/nn-casetup-imscepsetup">IMSCEPSetup</a>.

## -enum-fields

### -field ENUM_CEPSETUPPROP_USELOCALSYSTEM:0

A <b>VT_BOOL</b> value that specifies whether the Microsoft SCEP ISAPI Extension runs as the  local system user or under a separate user account. For remote CA or standalone CA configurations, by default this is set to <b>VARIANT_FALSE</b>. For a local enterprise CA configuration, by default this is set to <b>VARIANT_TRUE</b>.

### -field ENUM_CEPSETUPPROP_USECHALLENGE:1

A <b>VT_BOOL</b> value that specifies whether to require an SCEP challenge phrase to enroll. By default, setup sets this to <b>TRUE</b>.

### -field ENUM_CEPSETUPPROP_RANAME_CN:2

A <b>VT_BSTR</b> value that specifies the common name for Microsoft SCEP registration authority (RA) certificate name information. By default, the common name format is <i>MachineName</i>"-RA", where <i>MachineName</i> is the local machine name.

### -field ENUM_CEPSETUPPROP_RANAME_EMAIL:3

A <b>VT_BSTR</b> value that specifies an optional email address to be added in Microsoft SCEP RA certificate name information.

### -field ENUM_CEPSETUPPROP_RANAME_COMPANY:4

A <b>VT_BSTR</b> value that specifies an optional company name to be added in Microsoft SCEP RA certificate name information.

### -field ENUM_CEPSETUPPROP_RANAME_DEPT:5

A <b>VT_BSTR</b> value that specifies an optional department name to be added in Microsoft SCEP RA certificate name information.

### -field ENUM_CEPSETUPPROP_RANAME_CITY:6

A <b>VT_BSTR</b> value that specifies an optional city name to be added in Microsoft SCEP RA certificate name information.

### -field ENUM_CEPSETUPPROP_RANAME_STATE:7

A <b>VT_BSTR</b> value that specifies an optional state name to be added in Microsoft SCEP RA certificate name information.

### -field ENUM_CEPSETUPPROP_RANAME_COUNTRY:8

A <b>VT_BSTR</b> value that specifies the country or region name to be added in Microsoft SCEP RA certificate name information. By default, setup uses the country or region setting for the local computer.

### -field ENUM_CEPSETUPPROP_SIGNINGKEYINFORMATION:9

A <b>VT_IDISPATCH</b> value that is made up of an <a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetupkeyinformation">ICertSrvSetupKeyInformation</a> object used to create a Microsoft SCEP signing certificate. Setup creates a signing certificate based on an "EnrollmentAgentOffline" template.

### -field ENUM_CEPSETUPPROP_EXCHANGEKEYINFORMATION:10

A <b>VT_IDISPATCH</b> value that is made up of an <a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetupkeyinformation">ICertSrvSetupKeyInformation</a> object used to create a Microsoft SCEP key exchange certificate. Setup creates a key exchange certificate based on a "CEPEncryption" template.

### -field ENUM_CEPSETUPPROP_CAINFORMATION:11

A <b>VT_BSTR</b> value that specifies the Certification Authority (CA) information. By default, setup uses the local CA. If a local CA is present,  you should not set this property.

### -field ENUM_CEPSETUPPROP_MSCEPURL:12

A <b>VT_BSTR</b> value that specifies the URL for use by routers to connect and send certificate requests using SCEP. By default, setup uses http://<i>MachineName</i>/certsrv/mscep/mscep.dll, where <i>MachineName</i> is the local machine name. This is a read-only property.

### -field ENUM_CEPSETUPPROP_CHALLENGEURL:13

A <b>VT_BSTR</b> value that specifies the URL for use by router administrators to connect and obtain a challenge phrase. By default, setup uses http://<i>MachineName</i>/certsrv/mscep/, where <i>MachineName</i> is the local machine name. This is a read-only property.

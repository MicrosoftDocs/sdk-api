---
UID: NE:casetup.__MIDL___MIDL_itf_casetup_0000_0004_0001
title: "__MIDL___MIDL_itf_casetup_0000_0004_0001"
author: windows-sdk-content
description: Used by the GetProperty and SetProperty methods on the ICertificateEnrollmentServerSetup interface to specify the type of property information to retrieve or set.
old-location: security\cessetupproperty.htm
tech.root: seccrypto
ms.assetid: 9FA6B249-B5B3-40AF-B175-CD5933D468B9
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: CESSetupProperty, CESSetupProperty enumeration [Security], ENUM_CESSETUPPROP_AUTHENTICATION, ENUM_CESSETUPPROP_CACONFIG, ENUM_CESSETUPPROP_RENEWALONLY, ENUM_CESSETUPPROP_SSLCERTHASH, ENUM_CESSETUPPROP_URL, ENUM_CESSETUPPROP_USE_IISAPPPOOLIDENTITY, __MIDL___MIDL_itf_casetup_0000_0004_0001, casetup/CESSetupProperty, casetup/ENUM_CESSETUPPROP_AUTHENTICATION, casetup/ENUM_CESSETUPPROP_CACONFIG, casetup/ENUM_CESSETUPPROP_RENEWALONLY, casetup/ENUM_CESSETUPPROP_SSLCERTHASH, casetup/ENUM_CESSETUPPROP_URL, casetup/ENUM_CESSETUPPROP_USE_IISAPPPOOLIDENTITY, security.cessetupproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Casetup.h
api_name:
 - CESSetupProperty
product: Windows
targetos: Windows
req.typenames: CESSetupProperty
req.redist: 
---

# __MIDL___MIDL_itf_casetup_0000_0004_0001 enumeration


## -description


The <b>CESSetupProperty</b> enumeration type is used by the <a href="https://msdn.microsoft.com/4B380551-742C-4D36-80C9-C92F62F916BB">GetProperty</a> and <a href="https://msdn.microsoft.com/D2E20195-D81F-4717-83D2-BF8DC1D1779B">SetProperty</a> methods on the <a href="https://msdn.microsoft.com/B25DA7C4-0503-4E3B-BABC-6EFBD9EBDDAE">ICertificateEnrollmentServerSetup</a> interface to specify the type of property information to retrieve or set.


## -enum-fields




### -field ENUM_CESSETUPPROP_USE_IISAPPPOOLIDENTITY

The property value specifies whether the server context is <b>ApplicationPoolIdentity</b>.


### -field ENUM_CESSETUPPROP_CACONFIG

The property value contains a certification authority (CA) configuration string.


### -field ENUM_CESSETUPPROP_AUTHENTICATION

The property value specifies the type of authentication procedure used.


### -field ENUM_CESSETUPPROP_SSLCERTHASH

The property value contains a hash of the certificate used for authentication.


### -field ENUM_CESSETUPPROP_URL

The property value contains the Certificate Enrollment Web Service (CES) URL.


### -field ENUM_CESSETUPPROP_RENEWALONLY

The property value specifies whether CES can process only certificate renewals.


### -field ENUM_CESSETUPPROP_ALLOW_KEYBASED_RENEWAL




## -see-also




<a href="https://msdn.microsoft.com/4B380551-742C-4D36-80C9-C92F62F916BB">GetProperty</a>



<a href="https://msdn.microsoft.com/B25DA7C4-0503-4E3B-BABC-6EFBD9EBDDAE">ICertificateEnrollmentServerSetup</a>



<a href="https://msdn.microsoft.com/D2E20195-D81F-4717-83D2-BF8DC1D1779B">SetProperty</a>
 

 


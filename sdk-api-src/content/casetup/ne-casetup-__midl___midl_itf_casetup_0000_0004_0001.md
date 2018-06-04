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
 

 


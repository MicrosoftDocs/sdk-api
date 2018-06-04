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

# __MIDL___MIDL_itf_casetup_0000_0005_0001 enumeration


## -description


The <b>CEPSetupProperty</b> enumeration type is used by the <a href="https://msdn.microsoft.com/52AD50BB-4146-44FC-BA32-9FC46FFE32E4">GetProperty</a> and <a href="https://msdn.microsoft.com/81E20BFF-B4EC-4FA5-A881-5BDCE3FC3057">SetProperty</a> methods on the <a href="https://msdn.microsoft.com/8C9F33BA-5FCB-4B99-869C-FADDC37A326A">ICertificateEnrollmentPolicyServerSetup</a> interface to specify the type of property information to retrieve or set.


## -enum-fields




### -field ENUM_CEPSETUPPROP_AUTHENTICATION

The property value contains the type of authentication procedure used.


### -field ENUM_CEPSETUPPROP_SSLCERTHASH

The property value contains the hash of the certificate, if any, used for authentication.


### -field ENUM_CEPSETUPPROP_URL

The property value contains the Certificate Enrollment Policy (CEP) Web Service URL.


### -field ENUM_CEPSETUPPROP_KEYBASED_RENEWAL

The property value indicates  whether to set up the Enrollment Policy Server in a mode that returns policies for KeyBasedRenewal templates only.


## -see-also




<a href="https://msdn.microsoft.com/52AD50BB-4146-44FC-BA32-9FC46FFE32E4">GetProperty</a>



<a href="https://msdn.microsoft.com/8C9F33BA-5FCB-4B99-869C-FADDC37A326A">ICertificateEnrollmentPolicyServerSetup</a>



<a href="https://msdn.microsoft.com/81E20BFF-B4EC-4FA5-A881-5BDCE3FC3057">SetProperty</a>
 

 


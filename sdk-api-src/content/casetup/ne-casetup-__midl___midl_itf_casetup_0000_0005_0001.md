---
UID: NE:casetup.__MIDL___MIDL_itf_casetup_0000_0005_0001
title: "__MIDL___MIDL_itf_casetup_0000_0005_0001"
author: windows-sdk-content
description: Used by the GetProperty and SetProperty methods on the ICertificateEnrollmentPolicyServerSetup interface to specify the type of property information to retrieve or set.
old-location: security\cepsetupproperty.htm
old-project: SecCrypto
ms.assetid: 344701CA-089C-4152-BDA4-249728863180
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CEPSetupProperty, CEPSetupProperty enumeration [Security], ENUM_CEPSETUPPROP_AUTHENTICATION, ENUM_CEPSETUPPROP_KEYBASED_RENEWAL, ENUM_CEPSETUPPROP_SSLCERTHASH, ENUM_CEPSETUPPROP_URL, __MIDL___MIDL_itf_casetup_0000_0005_0001, casetup/CEPSetupProperty, casetup/ENUM_CEPSETUPPROP_AUTHENTICATION, casetup/ENUM_CEPSETUPPROP_KEYBASED_RENEWAL, casetup/ENUM_CEPSETUPPROP_SSLCERTHASH, casetup/ENUM_CEPSETUPPROP_URL, security.cepsetupproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CEPSetupProperty
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Casetup.h
api_name:
 - CEPSetupProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 


---
UID: NE:casetup.__MIDL___MIDL_itf_casetup_0000_0005_0001
title: CEPSetupProperty (casetup.h)
description: Used by the GetProperty and SetProperty methods on the ICertificateEnrollmentPolicyServerSetup interface to specify the type of property information to retrieve or set.helpviewer_keywords: ["CEPSetupProperty","CEPSetupProperty enumeration [Security]","ENUM_CEPSETUPPROP_AUTHENTICATION","ENUM_CEPSETUPPROP_KEYBASED_RENEWAL","ENUM_CEPSETUPPROP_SSLCERTHASH","ENUM_CEPSETUPPROP_URL","casetup/CEPSetupProperty","casetup/ENUM_CEPSETUPPROP_AUTHENTICATION","casetup/ENUM_CEPSETUPPROP_KEYBASED_RENEWAL","casetup/ENUM_CEPSETUPPROP_SSLCERTHASH","casetup/ENUM_CEPSETUPPROP_URL","security.cepsetupproperty"]
old-location: security\cepsetupproperty.htm
tech.root: SecCrypto
ms.assetid: 344701CA-089C-4152-BDA4-249728863180
ms.date: 12/05/2018
ms.keywords: CEPSetupProperty, CEPSetupProperty enumeration [Security], ENUM_CEPSETUPPROP_AUTHENTICATION, ENUM_CEPSETUPPROP_KEYBASED_RENEWAL, ENUM_CEPSETUPPROP_SSLCERTHASH, ENUM_CEPSETUPPROP_URL, casetup/CEPSetupProperty, casetup/ENUM_CEPSETUPPROP_AUTHENTICATION, casetup/ENUM_CEPSETUPPROP_KEYBASED_RENEWAL, casetup/ENUM_CEPSETUPPROP_SSLCERTHASH, casetup/ENUM_CEPSETUPPROP_URL, security.cepsetupproperty
f1_keywords:
- casetup/CEPSetupProperty
dev_langs:
- c++
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
- CEPSetupProperty
targetos: Windows
req.typenames: CEPSetupProperty
req.redist: 
ms.custom: 19H1
---

# CEPSetupProperty enumeration


## -description


The <b>CEPSetupProperty</b> enumeration type is used by the <a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-getproperty">GetProperty</a> and <a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-setproperty">SetProperty</a> methods on the <a href="https://docs.microsoft.com/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentpolicyserversetup">ICertificateEnrollmentPolicyServerSetup</a> interface to specify the type of property information to retrieve or set.


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




<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-getproperty">GetProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentpolicyserversetup">ICertificateEnrollmentPolicyServerSetup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentpolicyserversetup-setproperty">SetProperty</a>
 

 


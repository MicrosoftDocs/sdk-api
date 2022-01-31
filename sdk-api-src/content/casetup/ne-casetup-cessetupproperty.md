---
UID: NE:casetup.__MIDL___MIDL_itf_casetup_0000_0004_0001
title: CESSetupProperty (casetup.h)
description: Used by the GetProperty and SetProperty methods on the ICertificateEnrollmentServerSetup interface to specify the type of property information to retrieve or set.
helpviewer_keywords: ["CESSetupProperty","CESSetupProperty enumeration [Security]","ENUM_CESSETUPPROP_AUTHENTICATION","ENUM_CESSETUPPROP_CACONFIG","ENUM_CESSETUPPROP_RENEWALONLY","ENUM_CESSETUPPROP_SSLCERTHASH","ENUM_CESSETUPPROP_URL","ENUM_CESSETUPPROP_USE_IISAPPPOOLIDENTITY","casetup/CESSetupProperty","casetup/ENUM_CESSETUPPROP_AUTHENTICATION","casetup/ENUM_CESSETUPPROP_CACONFIG","casetup/ENUM_CESSETUPPROP_RENEWALONLY","casetup/ENUM_CESSETUPPROP_SSLCERTHASH","casetup/ENUM_CESSETUPPROP_URL","casetup/ENUM_CESSETUPPROP_USE_IISAPPPOOLIDENTITY","security.cessetupproperty"]
old-location: security\cessetupproperty.htm
tech.root: security
ms.assetid: 9FA6B249-B5B3-40AF-B175-CD5933D468B9
ms.date: 12/05/2018
ms.keywords: CESSetupProperty, CESSetupProperty enumeration [Security], ENUM_CESSETUPPROP_AUTHENTICATION, ENUM_CESSETUPPROP_CACONFIG, ENUM_CESSETUPPROP_RENEWALONLY, ENUM_CESSETUPPROP_SSLCERTHASH, ENUM_CESSETUPPROP_URL, ENUM_CESSETUPPROP_USE_IISAPPPOOLIDENTITY, casetup/CESSetupProperty, casetup/ENUM_CESSETUPPROP_AUTHENTICATION, casetup/ENUM_CESSETUPPROP_CACONFIG, casetup/ENUM_CESSETUPPROP_RENEWALONLY, casetup/ENUM_CESSETUPPROP_SSLCERTHASH, casetup/ENUM_CESSETUPPROP_URL, casetup/ENUM_CESSETUPPROP_USE_IISAPPPOOLIDENTITY, security.cessetupproperty
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
targetos: Windows
req.typenames: CESSetupProperty
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_casetup_0000_0004_0001
 - casetup/__MIDL___MIDL_itf_casetup_0000_0004_0001
 - CESSetupProperty
 - casetup/CESSetupProperty
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
 - CESSetupProperty
---

# CESSetupProperty enumeration


## -description

The <b>CESSetupProperty</b> enumeration type is used by the <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-getproperty">GetProperty</a> and <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-setproperty">SetProperty</a> methods on the <a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentserversetup">ICertificateEnrollmentServerSetup</a> interface to specify the type of property information to retrieve or set.

## -enum-fields

### -field ENUM_CESSETUPPROP_USE_IISAPPPOOLIDENTITY:0

The property value specifies whether the server context is <b>ApplicationPoolIdentity</b>.

### -field ENUM_CESSETUPPROP_CACONFIG:1

The property value contains a certification authority (CA) configuration string.

### -field ENUM_CESSETUPPROP_AUTHENTICATION:2

The property value specifies the type of authentication procedure used.

### -field ENUM_CESSETUPPROP_SSLCERTHASH:3

The property value contains a hash of the certificate used for authentication.

### -field ENUM_CESSETUPPROP_URL:4

The property value contains the Certificate Enrollment Web Service (CES) URL.

### -field ENUM_CESSETUPPROP_RENEWALONLY:5

The property value specifies whether CES can process only certificate renewals.

### -field ENUM_CESSETUPPROP_ALLOW_KEYBASED_RENEWAL:6

## -see-also

<a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-getproperty">GetProperty</a>



<a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentserversetup">ICertificateEnrollmentServerSetup</a>



<a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-setproperty">SetProperty</a>

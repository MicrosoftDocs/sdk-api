---
UID: NS:wincrypt._CERT_OR_CRL_BUNDLE
title: CERT_OR_CRL_BUNDLE (wincrypt.h)
author: windows-sdk-content
description: Encapsulates an array of certificates for use with Internet Key Exchange messages.
old-location: security\cert_or_crl_bundle.htm
tech.root: SecCrypto
ms.assetid: a06e71b4-63c7-4d4a-820c-e5901015aaa6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCERT_OR_CRL_BUNDLE, CERT_OR_CRL_BUNDLE, CERT_OR_CRL_BUNDLE structure [Security], PCERT_OR_CRL_BUNDLE, PCERT_OR_CRL_BUNDLE structure pointer [Security], security.cert_or_crl_bundle, wincrypt/CERT_OR_CRL_BUNDLE, wincrypt/PCERT_OR_CRL_BUNDLE"
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_OR_CRL_BUNDLE
product: Windows
targetos: Windows
req.typenames: CERT_OR_CRL_BUNDLE, *PCERT_OR_CRL_BUNDLE
req.redist: 
---

# CERT_OR_CRL_BUNDLE structure


## -description


The <b>CERT_OR_CRL_BUNDLE</b> structure encapsulates an array of certificates for use with Internet Key Exchange  messages.


## -struct-fields




### -field cItem

The number of items in the array pointed to by the <b>rgItem</b> member.


### -field rgItem

A pointer to an array of certificates.


---
UID: NF:wincrypt.CertFindExtension
title: CertFindExtension function (wincrypt.h)
description: The CertFindExtension function finds the first extension in the CERT_EXTENSION array, as identified by its object identifier (OID).
helpviewer_keywords: ["CertFindExtension","CertFindExtension function [Security]","_crypto2_certfindextension","security.certfindextension","wincrypt/CertFindExtension"]
old-location: security\certfindextension.htm
tech.root: security
ms.assetid: 489c58b6-a704-4f54-bc64-34eacafc347c
ms.date: 12/05/2018
ms.keywords: CertFindExtension, CertFindExtension function [Security], _crypto2_certfindextension, security.certfindextension, wincrypt/CertFindExtension
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertFindExtension
 - wincrypt/CertFindExtension
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertFindExtension
---

# CertFindExtension function


## -description

The <b>CertFindExtension</b> function finds the first extension in the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> array, as identified by its <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID). This function can be used in the processing of a decoded certificate. A 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure is derived from a decoded certificate. The <b>CERT_INFO</b> structure's <b>rgExtension</b> member is  passed to <b>CertFindExtension</b> in the <i>rgExtensions</i> parameter. This function determines whether a particular extension is in the array, and if so, returns a pointer to it

## -parameters

### -param pszObjId [in]

A pointer to the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) to use in the search.

### -param cExtensions [in]

Number of extensions in the <i>rgExtensions</i> array.

### -param rgExtensions [in]

Array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structures.

## -returns

Returns a pointer to the extension, if one is found. Otherwise, <b>NULL</b> is returned.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindattribute">CertFindAttribute</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindrdnattr">CertFindRDNAttr</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>
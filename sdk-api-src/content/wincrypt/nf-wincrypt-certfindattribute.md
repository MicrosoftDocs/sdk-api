---
UID: NF:wincrypt.CertFindAttribute
title: CertFindAttribute function (wincrypt.h)
description: The CertFindAttribute function finds the first attribute in the CRYPT_ATTRIBUTE array, as identified by its object identifier (OID).
helpviewer_keywords: ["CertFindAttribute","CertFindAttribute function [Security]","_crypto2_certfindattribute","security.certfindattribute","wincrypt/CertFindAttribute"]
old-location: security\certfindattribute.htm
tech.root: security
ms.assetid: 99d690fb-ea85-4cb1-9fb0-bdb02e4ac50a
ms.date: 12/05/2018
ms.keywords: CertFindAttribute, CertFindAttribute function [Security], _crypto2_certfindattribute, security.certfindattribute, wincrypt/CertFindAttribute
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
 - CertFindAttribute
 - wincrypt/CertFindAttribute
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
 - CertFindAttribute
---

# CertFindAttribute function


## -description

The <b>CertFindAttribute</b> function finds the first attribute in the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a> array, as identified by its <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID). This function can be used in the processing of a decoded <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>. A 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_request_info">CERT_REQUEST_INFO</a> structure is derived from a decoded certificate request. The <b>rgAttribute</b> array is retrieved from that structure and passed to this function in the <i>rgAttr</i> parameter. This function determines whether a particular attribute is in the array, and if so, returns a pointer to it.

## -parameters

### -param pszObjId [in]

A pointer to the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) to use in the search.

### -param cAttr [in]

Number of attributes in the <i>rgAttr</i> array.

### -param rgAttr [in]

Array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a> structures.

## -returns

Returns a pointer to the attribute, if one is found. Otherwise, <b>NULL</b> is returned.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindextension">CertFindExtension</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindrdnattr">CertFindRDNAttr</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>
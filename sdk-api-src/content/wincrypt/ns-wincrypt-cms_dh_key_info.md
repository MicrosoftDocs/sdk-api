---
UID: NS:wincrypt._CMS_DH_KEY_INFO
title: CMS_DH_KEY_INFO (wincrypt.h)
description: Used with the KP_CMS_DH_KEY_INFO parameter in the CryptSetKeyParam function to contain Diffie-Hellman key information.
helpviewer_keywords: ["*PCMS_DH_KEY_INFO","CMS_DH_KEY_INFO","CMS_DH_KEY_INFO structure [Security]","PCMS_DH_KEY_INFO","PCMS_DH_KEY_INFO structure pointer [Security]","security.cms_dh_key_info","wincrypt/CMS_DH_KEY_INFO","wincrypt/PCMS_DH_KEY_INFO"]
old-location: security\cms_dh_key_info.htm
tech.root: security
ms.assetid: ecfd8a63-95f9-4026-b31b-671ea58b683f
ms.date: 12/05/2018
ms.keywords: '*PCMS_DH_KEY_INFO, CMS_DH_KEY_INFO, CMS_DH_KEY_INFO structure [Security], PCMS_DH_KEY_INFO, PCMS_DH_KEY_INFO structure pointer [Security], security.cms_dh_key_info, wincrypt/CMS_DH_KEY_INFO, wincrypt/PCMS_DH_KEY_INFO'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: CMS_DH_KEY_INFO, *PCMS_DH_KEY_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMS_DH_KEY_INFO
 - wincrypt/_CMS_DH_KEY_INFO
 - PCMS_DH_KEY_INFO
 - wincrypt/PCMS_DH_KEY_INFO
 - CMS_DH_KEY_INFO
 - wincrypt/CMS_DH_KEY_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMS_DH_KEY_INFO
---

# CMS_DH_KEY_INFO structure


## -description

The <b>CMS_DH_KEY_INFO</b> structure is used with the <b>KP_CMS_DH_KEY_INFO</b> parameter in the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyparam">CryptSetKeyParam</a> function to contain <a href="/windows/desktop/SecGloss/d-gly">Diffie-Hellman</a> key information.

## -struct-fields

### -field dwVersion

The size, in bytes, of this structure.

### -field Algid

One of the <a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a> values that identifies the algorithm for the key to be converted.

### -field pszContentEncObjId

The address of a null-terminated ANSI string that contains the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of the content encryption algorithm.

### -field PubInfo

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains additional public information. This member is optional and the <b>cbData</b> member of this structure can be zero if this is not needed.

### -field pReserved

Reserved for future use and must be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsetkeyparam">CryptSetKeyParam</a>
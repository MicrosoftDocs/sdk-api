---
UID: NS:wincrypt._CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA
title: CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA (wincrypt.h)
description: Used with the CryptInstallDefaultContext function to contain an array of object identifier strings.
helpviewer_keywords: ["*PCRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA","CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA","CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA structure [Security]","PCRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA","PCRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA structure pointer [Security]","security.crypt_default_context_multi_oid_para","wincrypt/CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA","wincrypt/PCRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA"]
old-location: security\crypt_default_context_multi_oid_para.htm
tech.root: security
ms.assetid: 2826ee4f-55b7-4161-8698-3a9b59190dcc
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA, CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA, CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA structure [Security], PCRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA, PCRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA structure pointer [Security], security.crypt_default_context_multi_oid_para, wincrypt/CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA, wincrypt/PCRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA'
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
req.typenames: CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA, *PCRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA
 - wincrypt/_CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA
 - PCRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA
 - wincrypt/PCRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA
 - CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA
 - wincrypt/CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA
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
 - CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA
---

# CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA structure


## -description

The <b>CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA</b> structure is used with the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptinstalldefaultcontext">CryptInstallDefaultContext</a> function to contain an array of object identifier strings.

## -struct-fields

### -field cOID

The number of elements in the <b>rgpszOID</b> array.

### -field rgpszOID

An array of pointers to null-terminated ANSI strings that contain the object identifier strings of the certificate signature algorithm to install the default provider for, for example, <b>szOID_OIWSEC_md5RSA</b>. The <b>cOID</b> member of this structure contains the number of elements in this array.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptinstalldefaultcontext">CryptInstallDefaultContext</a>
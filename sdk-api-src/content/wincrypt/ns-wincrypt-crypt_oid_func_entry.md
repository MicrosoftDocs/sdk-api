---
UID: NS:wincrypt._CRYPT_OID_FUNC_ENTRY
title: CRYPT_OID_FUNC_ENTRY (wincrypt.h)
author: windows-sdk-content
description: Contains an object identifier (OID) and a pointer to its related function.
old-location: security\crypt_oid_func_entry.htm
tech.root: SecCrypto
ms.assetid: 84c4aca8-ee38-455f-8330-58f512a6d12c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCRYPT_OID_FUNC_ENTRY, CRYPT_OID_FUNC_ENTRY, CRYPT_OID_FUNC_ENTRY structure [Security], PCRYPT_OID_FUNC_ENTRY, PCRYPT_OID_FUNC_ENTRY structure pointer [Security], _crypto2_crypt_oid_func_entry, security.crypt_oid_func_entry, wincrypt/CRYPT_OID_FUNC_ENTRY, wincrypt/PCRYPT_OID_FUNC_ENTRY"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_OID_FUNC_ENTRY
product: Windows
targetos: Windows
req.typenames: CRYPT_OID_FUNC_ENTRY, *PCRYPT_OID_FUNC_ENTRY
req.redist: 
ms.custom: 19H1
---

# CRYPT_OID_FUNC_ENTRY structure


## -description


The <b>CRYPT_OID_FUNC_ENTRY</b> structure contains an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) and a pointer to its related function. It is used with 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress">CryptInstallOIDFunctionAddress</a>.


## -struct-fields




### -field pszOID

If the high-order word of the OID is nonzero, <b>pszOID</b> is a pointer to either an OID string, such as "2.5.29.1" or an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">ASCII</a> string, such as "file". If the high-order word of the OID is zero, the low-order word specifies the numeric identifier to be used as the object identifier.


### -field pvFuncAddr

The starting address of the function that the OID identifies.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress">CryptInstallOIDFunctionAddress</a>
 

 


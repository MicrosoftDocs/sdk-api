---
UID: NS:wincrypt._CRYPT_OID_FUNC_ENTRY
title: "_CRYPT_OID_FUNC_ENTRY"
author: windows-sdk-content
description: Contains an object identifier (OID) and a pointer to its related function.
old-location: security\crypt_oid_func_entry.htm
old-project: SecCrypto
ms.assetid: 84c4aca8-ee38-455f-8330-58f512a6d12c
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: "*PCRYPT_OID_FUNC_ENTRY, CRYPT_OID_FUNC_ENTRY, CRYPT_OID_FUNC_ENTRY structure [Security], PCRYPT_OID_FUNC_ENTRY, PCRYPT_OID_FUNC_ENTRY structure pointer [Security], _CRYPT_OID_FUNC_ENTRY, _crypto2_crypt_oid_func_entry, security.crypt_oid_func_entry, wincrypt/CRYPT_OID_FUNC_ENTRY, wincrypt/PCRYPT_OID_FUNC_ENTRY"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CRYPT_OID_FUNC_ENTRY, *PCRYPT_OID_FUNC_ENTRY
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRYPT_OID_FUNC_ENTRY structure


## -description


The <b>CRYPT_OID_FUNC_ENTRY</b> structure contains an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) and a pointer to its related function. It is used with 
<a href="https://msdn.microsoft.com/934e8278-0e0b-4402-a2b6-ff1e913d54c9">CryptInstallOIDFunctionAddress</a>.


## -struct-fields




### -field pszOID

If the high-order word of the OID is nonzero, <b>pszOID</b> is a pointer to either an OID string, such as "2.5.29.1" or an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ASCII</a> string, such as "file". If the high-order word of the OID is zero, the low-order word specifies the numeric identifier to be used as the object identifier.


### -field pvFuncAddr

The starting address of the function that the OID identifies.


## -see-also




<a href="https://msdn.microsoft.com/934e8278-0e0b-4402-a2b6-ff1e913d54c9">CryptInstallOIDFunctionAddress</a>
 

 


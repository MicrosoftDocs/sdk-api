---
UID: NS:wincrypt._CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA
title: "_CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA"
author: windows-sdk-content
description: Used with the CryptInstallDefaultContext function to contain an array of object identifier strings.
old-location: security\crypt_default_context_multi_oid_para.htm
old-project: seccrypto
ms.assetid: 2826ee4f-55b7-4161-8698-3a9b59190dcc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PCRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA, CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA, CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA structure [Security], PCRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA, PCRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA structure pointer [Security], _CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA, security.crypt_default_context_multi_oid_para, wincrypt/CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA, wincrypt/PCRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA"
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
req.typenames: CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA, *PCRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA structure


## -description


The <b>CRYPT_DEFAULT_CONTEXT_MULTI_OID_PARA</b> structure is used with the <a href="https://msdn.microsoft.com/79d121df-0699-424e-a8de-5fc2b396afc2">CryptInstallDefaultContext</a> function to contain an array of object identifier strings.


## -struct-fields




### -field cOID

The number of elements in the <b>rgpszOID</b> array.


### -field rgpszOID

An array of pointers to null-terminated ANSI strings that contain the object identifier strings of the certificate signature algorithm to install the default provider for, for example, <b>szOID_OIWSEC_md5RSA</b>. The <b>cOID</b> member of this structure contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/79d121df-0699-424e-a8de-5fc2b396afc2">CryptInstallDefaultContext</a>
 

 


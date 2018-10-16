---
UID: NS:wincrypt._CRYPT_KEY_PROV_PARAM
title: "_CRYPT_KEY_PROV_PARAM"
author: windows-sdk-content
description: Contains information about a key container parameter.
old-location: security\crypt_key_prov_param.htm
tech.root: seccrypto
ms.assetid: 3731708f-0ce9-42bf-ace9-5ed671be113a
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PCRYPT_KEY_PROV_PARAM, CRYPT_KEY_PROV_PARAM, CRYPT_KEY_PROV_PARAM structure [Security], PCRYPT_KEY_PROV_PARAM, PCRYPT_KEY_PROV_PARAM structure pointer [Security], _CRYPT_KEY_PROV_PARAM, _crypto2_crypt_key_prov_param, security.crypt_key_prov_param, wincrypt/CRYPT_KEY_PROV_PARAM, wincrypt/PCRYPT_KEY_PROV_PARAM"
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
 - CRYPT_KEY_PROV_PARAM
product: Windows
targetos: Windows
req.typenames: CRYPT_KEY_PROV_PARAM, *PCRYPT_KEY_PROV_PARAM
req.redist: 
---

# _CRYPT_KEY_PROV_PARAM structure


## -description


The <b>CRYPT_KEY_PROV_PARAM</b> structure contains information about a <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key container</a> parameter. This structure is used with the 
<a href="https://msdn.microsoft.com/6aea2f47-9d4a-4069-ac6d-f28907df00be">CRYPT_KEY_PROV_INFO</a> structure.


## -struct-fields




### -field dwParam

Identifies the parameter. For possible values, see the <i>dwParam</i> parameter of the 
<a href="https://msdn.microsoft.com/98306a7b-b218-4eb4-99f0-0b5bcc632a13">CryptSetProvParam</a> function.


### -field pbData

The address of a buffer that contains the parameter data. For more information, see the <i>pbData</i> parameter of the 
<a href="https://msdn.microsoft.com/98306a7b-b218-4eb4-99f0-0b5bcc632a13">CryptSetProvParam</a> function.


### -field cbData

The size, in bytes, of the <b>pbData</b> buffer.


### -field dwFlags

This member is reserved for future use and is zero.


## -see-also




<a href="https://msdn.microsoft.com/6aea2f47-9d4a-4069-ac6d-f28907df00be">CRYPT_KEY_PROV_INFO</a>



<a href="https://msdn.microsoft.com/98306a7b-b218-4eb4-99f0-0b5bcc632a13">CryptSetProvParam</a>
 

 


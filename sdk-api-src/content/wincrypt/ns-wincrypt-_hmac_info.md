---
UID: NS:wincrypt._HMAC_Info
title: "_HMAC_Info"
author: windows-sdk-content
description: The HMAC_INFO structure specifies the hash algorithm and the inner and outer strings that are to be used to calculate the HMAC hash.
old-location: security\hmac_info.htm
tech.root: seccrypto
ms.assetid: 0c9a9b60-077d-48c0-a5a6-01640cfc0c4e
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: "*PHMAC_INFO, HMAC_INFO, HMAC_INFO structure [Security], PHMAC_INFO, PHMAC_INFO structure pointer [Security], _HMAC_Info, _crypto2_hmac_info, security.hmac_info, wincrypt/HMAC_INFO, wincrypt/PHMAC_INFO"
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
 - HMAC_INFO
product: Windows
targetos: Windows
req.typenames: HMAC_INFO, *PHMAC_INFO
req.redist: 
---

# _HMAC_Info structure


## -description


The <b>HMAC_INFO</b> structure specifies the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">hash</a> algorithm and the inner and outer strings that are to be used to calculate the <a href="https://msdn.microsoft.com/4165b820-30fc-477e-a690-81109f161323">HMAC</a> hash.


## -struct-fields




### -field HashAlgid

Specifies the hash algorithm to be used.


### -field pbInnerString

A pointer to the inner string to be used in the HMAC calculation. The default inner string is defined as the byte 0x36 repeated 64 times.


### -field cbInnerString

The count of bytes in <b>pbInnerString</b>. The CSP uses the default inner string if <b>cbInnerString</b> is equal to zero.


### -field pbOuterString

A pointer to the outer string to be used in the HMAC calculation. The default outer string is defined as the byte 0x5C repeated 64 times.


### -field cbOuterString

The count of bytes in <b>pbOuterString</b>. The CSP uses the default outer string if <b>cbOuterString</b> is equal to zero.


## -see-also




<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>



<a href="https://msdn.microsoft.com/05e3db57-8d83-48e2-8590-68039ea27253">CryptCreateHash</a>



<a href="https://msdn.microsoft.com/0c8d3ef9-e7b5-4e49-a2f8-9c85b16549da">CryptSetHashParam</a>
 

 


---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 


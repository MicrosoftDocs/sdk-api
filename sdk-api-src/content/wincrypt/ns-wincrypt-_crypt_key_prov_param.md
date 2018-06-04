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
 

 


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

# CryptXmlSetHMACSecret function


## -description


The <b>CryptXmlSetHMACSecret</b> function sets the HMAC secret on the handle before
 calling the <a href="https://msdn.microsoft.com/38bd365e-bc63-498c-a650-471429f09d37">CryptXmlSign</a> or <a href="https://msdn.microsoft.com/1f8776dc-d91a-4be9-90bf-7d36d587ffb2">CryptXmlVerify</a> function.


## -parameters




### -param hSignature [in]

The handle of the XML <b>Signature</b> element.


### -param pbSecret [in]

A pointer to a buffer that contains a block of bytes. 
    The pointer must be valid during the call to the <a href="https://msdn.microsoft.com/38bd365e-bc63-498c-a650-471429f09d37">CryptXmlSign</a> or <a href="https://msdn.microsoft.com/1f8776dc-d91a-4be9-90bf-7d36d587ffb2">CryptXmlVerify</a> function.


### -param cbSecret

The size, in bytes, of the buffer pointed to by the <i>pbSecret</i> parameter. 


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.




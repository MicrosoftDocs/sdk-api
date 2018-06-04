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

# ICertEncodeBitString::GetBitCount


## -description


The <b>GetBitCount</b> method returns the number of bits in a bit string that belongs to the 
<a href="https://msdn.microsoft.com/51178b67-46da-49f8-9bd7-a500e846e0a8">CertEncodeBitString</a> object and has been initialized by an earlier call to 
<a href="https://msdn.microsoft.com/65856db4-97db-4c9b-ac12-1a9262c7b4e9">ICertEncodeBitString::Decode</a>.


## -parameters




### -param pBitCount [out]

A pointer to a <b>Long</b> that will receive the number of bits in the bit string.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the number of bits in the bit string.




## -see-also




<a href="https://msdn.microsoft.com/51178b67-46da-49f8-9bd7-a500e846e0a8">ICertEncodeBitString</a>
 

 


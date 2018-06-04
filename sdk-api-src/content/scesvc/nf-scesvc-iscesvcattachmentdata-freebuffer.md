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

# ISceSvcAttachmentData::FreeBuffer


## -description


The <b>FreeBuffer</b> method frees memory allocated by the Security Configuration snap-in.


## -parameters




### -param pvData [in]

Void pointer to the buffer to be freed.


## -returns



The return value is an HRESULT. A value of S_OK indicates the method was successful.




## -remarks



You should call this method to free the data buffer returned by 
<a href="https://msdn.microsoft.com/f0b51592-58d9-45f2-a0a5-7cdbde0bc0a1">ISceSvcAttachmentData::GetData</a>.




## -see-also




<a href="https://msdn.microsoft.com/385acdb9-5642-47c1-b2ac-be388edaac12">ISceSvcAttachmentData</a>



<a href="https://msdn.microsoft.com/f0b51592-58d9-45f2-a0a5-7cdbde0bc0a1">ISceSvcAttachmentData::GetData</a>
 

 


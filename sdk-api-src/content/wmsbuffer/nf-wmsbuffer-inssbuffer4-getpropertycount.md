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

# INSSBuffer4::GetPropertyCount


## -description



The <b>GetPropertyCount</b> method retrieves the total number of buffer properties, also called data unit extensions, associated with the sample contained in the buffer object. When using <a href="https://msdn.microsoft.com/8812b7c9-610b-4c17-a274-55e043cfb091">INSSBuffer4::GetPropertyByIndex</a> to retrieve properties, the index used is between zero and the number specified by this method.




## -parameters




### -param pcBufferProperties [out]

Pointer to the size of buffer properties.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d6531e52-b58b-46ed-a47b-444cd98e1ec5">INSSBuffer4 Interface</a>
 

 


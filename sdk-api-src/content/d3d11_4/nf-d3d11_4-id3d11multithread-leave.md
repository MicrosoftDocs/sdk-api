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

# ID3D11Multithread::Leave


## -description


Leave a device's critical section.


## -parameters






## -returns



This method does not return a value.




## -remarks



This function is typically used in multithreaded applications when there is a series of graphics commands 
		  that must happen in order. <a href="https://msdn.microsoft.com/A742D03A-0A47-4B08-952A-836A272D1519">Enter</a> is typically called at the beginning of a series of graphics commands, and this function is typically 
		  called after those graphics commands.




## -see-also




<a href="https://msdn.microsoft.com/1A07694E-7D61-4A59-82E3-048F04C8D57A">ID3D11Multithread</a>
 

 


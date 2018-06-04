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

# AVIStreamGetFrame function


## -description



The <b>AVIStreamGetFrame</b> function returns the address of a decompressed video frame.




## -parameters




### -param pg

TBD


### -param lPos

Position, in samples, within the stream of the desired frame.


#### - pgf

Pointer to the <a href="https://msdn.microsoft.com/d72349bc-5e7c-4c60-b8e0-0524d02c0583">IGetFrame</a> interface.


## -returns



Returns a pointer to the frame data if successful or <b>NULL</b> otherwise. The frame data is returned as a packed DIB.




## -remarks



The returned frame is valid only until the next call to this function or the <a href="https://msdn.microsoft.com/cd1fa615-ab09-4d58-9d6d-a1843c0f1d7a">AVIStreamGetFrameClose</a> function.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 


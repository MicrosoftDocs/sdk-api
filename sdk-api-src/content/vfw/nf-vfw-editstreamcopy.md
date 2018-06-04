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

# EditStreamCopy function


## -description



The <b>EditStreamCopy</b> function copies an editable stream (or a portion of it) into a temporary stream.




## -parameters




### -param pavi

Handle to the stream being copied.


### -param plStart

Starting position within the stream being copied. The starting position is returned.


### -param plLength

Amount of data to copy from the stream referenced by <i>pavi</i>. The length of the copied data is returned.


### -param ppResult

Pointer to a buffer that receives the handle created for the new stream.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



The stream that is copied must be created by the <b>CreateEditableStream</b> function or one of the stream editing functions.

The temporary stream can be treated as any other AVI stream.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 


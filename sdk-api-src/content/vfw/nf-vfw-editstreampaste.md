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

# EditStreamPaste function


## -description



The <b>EditStreamPaste</b> function copies a stream (or a portion of it) from one stream and pastes it within another stream at a specified location.




## -parameters




### -param pavi

Handle to an editable stream that will receive the copied stream data.


### -param plPos

Starting position to paste the data within the destination stream (referenced by <i>pavi</i>).


### -param plLength

Pointer to a buffer that receives the amount of data pasted in the stream.


### -param pstream

Handle to a stream supplying the data to paste. This stream does not need to be an editable stream.


### -param lStart

Starting position of the data to copy within the source stream.


### -param lEnd

TBD




#### - lLength

Amount of data to copy from the source stream. If <i>lLength</i> is -1, the entire stream referenced by <i>pstream</i> is pasted in the other stream.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



The stream referenced by <i>pavi</i> must have been created by the <b>CreateEditableStream</b> function or one of the stream editing functions.

This function inserts data into the specified stream as a continuous block of data. It opens the specified data stream at the insertion point, pastes the specified stream segment at the insertion point, and appends the stream segment that trails the insertion point to the end of pasted segment.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/97ab491d-1a58-4b4b-a13a-215be24dac1c">Positioning in Streams</a>
 

 


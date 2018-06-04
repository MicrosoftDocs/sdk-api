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

# AVIFileWriteData function


## -description



The <b>AVIFileWriteData</b> function writes supplementary data (other than normal header, format, and stream data) to the file.




## -parameters




### -param pfile

Handle to an open AVI file.


### -param ckid

RIFF chunk identifier (four-character code) of the data.


### -param lpData

Pointer to the buffer used to write the data.


### -param cbData

Size, in bytes, of the memory block referenced by <i>lpData</i>.


## -returns



Returns zero if successful or an error otherwise. In an application has read-only access to the file, the error code AVIERR_READONLY is returned.




## -remarks



Use the <a href="https://msdn.microsoft.com/2ca91df6-4721-4282-8b88-81e76d2ab94f">AVIStreamWriteData</a> function to write data that applies to an individual stream.

The argument <i>pfile</i> is a pointer to an <a href="https://msdn.microsoft.com/401db941-cbf6-452b-84e2-605fafac8a6d">IAVIFile</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 


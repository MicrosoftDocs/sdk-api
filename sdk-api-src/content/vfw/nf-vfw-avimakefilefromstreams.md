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

# AVIMakeFileFromStreams function


## -description



The <b>AVIMakeFileFromStreams</b> function constructs an AVIFile interface pointer from separate streams.




## -parameters




### -param ppfile

Pointer to a buffer that receives the new file interface pointer.


### -param nStreams

Count of the number of streams in the array of stream interface pointers referenced by papStreams.


### -param papStreams

Pointer to an array of stream interface pointers.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



Use the <a href="https://msdn.microsoft.com/c2f94ca2-b46c-48b0-9c31-92cf2cf75be3">AVIFileRelease</a> function to close the file.

Other functions can use the AVIFile interface created by this function to copy and edit the streams associated with the interface. For example, you can retrieve a specific stream by using <a href="https://msdn.microsoft.com/b51a823c-6904-4942-883f-bda347541757">AVIFileGetStream</a> with the file interface pointer.

The argument <i>pfile</i> is the address of a pointer to an <a href="https://msdn.microsoft.com/401db941-cbf6-452b-84e2-605fafac8a6d">IAVIFile</a> interface. The argument <i>papStreams</i> is the address of a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/b51a823c-6904-4942-883f-bda347541757">AVIFileGetStream</a>



<a href="https://msdn.microsoft.com/c2f94ca2-b46c-48b0-9c31-92cf2cf75be3">AVIFileRelease</a>
 

 


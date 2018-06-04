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

# _tag_AMVABeginFrameInfo structure


## -description



          The <b>AMVABeginFrameInfo</b> structure contains information for the <a href="https://msdn.microsoft.com/00077ffe-4acb-4648-9e95-652184e4449b">IAMVideoAccelerator::BeginFrame</a> method.


## -struct-fields




### -field dwDestSurfaceIndex

The zero-based index of the uncompressed destination surface. The number of uncompressed surfaces is specified in the <a href="https://msdn.microsoft.com/e82c73e6-d32e-4875-9f9d-124a1c6ce504">IAMVideoAcceleratorNotify::SetUncompSurfacesInfo</a> method.


### -field pInputData


            Pointer to a buffer that contains data for the video accelerator.

This buffer must contain a <b>WORD</b> value that is equal to the value of <b>dwDestSurfaceIndex</b>.


### -field dwSizeInputData


            Size, in bytes, of the buffer that <b>pInputData</b> points to. The value must be 2.


### -field pOutputData


            Pointer to a buffer that the video accelerator can write to.

This member must be <b>NULL</b>.


### -field dwSizeOutputData


            Size, in bytes, of the buffer that <b>pOutputData</b> points to. The value must be zero.


## -remarks




        The buffer pointed to by <b>pInputData</b> cannot contain pointer values, because their addresses will not be valid in kernel mode, where frame processing occurs.
      


        The video accelerator might not use the same surface memory in two consecutive calls with the same frame index.
      Therefore, the decoder should not make any assumption about the initial contents of the frame.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/00077ffe-4acb-4648-9e95-652184e4449b">IAMVideoAccelerator::BeginFrame</a>
 

 


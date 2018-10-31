---
UID: NE:vmr9._VMR9_SampleFormat
title: "_VMR9_SampleFormat"
author: windows-sdk-content
description: The VMR9_SampleFormat enumeration type describes the interlacing of a video stream.
old-location: dshow\vmr9_sampleformat.htm
tech.root: DirectShow
ms.assetid: 0e501c05-91ac-4594-bdfe-e8b4bfeb5bcb
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: VMR9_SampleFieldInterleavedEvenFirst, VMR9_SampleFieldInterleavedOddFirst, VMR9_SampleFieldSingleEven, VMR9_SampleFieldSingleOdd, VMR9_SampleFormat, VMR9_SampleFormat , VMR9_SampleFormat enumeration [DirectShow], VMR9_SampleProgressiveFrame, VMR9_SampleReserved, _VMR9_SampleFormat, dshow.vmr9_sampleformat, vmr9/VMR9_SampleFieldInterleavedEvenFirst, vmr9/VMR9_SampleFieldInterleavedOddFirst, vmr9/VMR9_SampleFieldSingleEven, vmr9/VMR9_SampleFieldSingleOdd, vmr9/VMR9_SampleFormat, vmr9/VMR9_SampleProgressiveFrame, vmr9/VMR9_SampleReserved
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmr9.h
api_name:
 - VMR9_SampleFormat
product: Windows
targetos: Windows
req.typenames: VMR9_SampleFormat
req.redist: 
---

# _VMR9_SampleFormat enumeration


## -description



The <b>VMR9_SampleFormat</b> enumeration type describes the interlacing of a video stream.




## -enum-fields




### -field VMR9_SampleReserved

Reserved; do not use.
          


### -field VMR9_SampleProgressiveFrame

Progressive frame; no interleaving
          


### -field VMR9_SampleFieldInterleavedEvenFirst

Each sample contains two interleaved fields, with the even field first.
          


### -field VMR9_SampleFieldInterleavedOddFirst

Each sample contains two interleaved fields, with the odd field first.
          


### -field VMR9_SampleFieldSingleEven

The sample contains a single field, and each line in the sample corresponds to the even lines in a deinterlaced frame. That is, lines 0, 1, 2,... in the sample correspond to lines 0, 2, 4,... in the deinterlaced frame. The missing lines must be constructed when the frame is deinterlaced.
          


### -field VMR9_SampleFieldSingleOdd

The sample contains a single field, and each line in the sample corresponds to the odd lines in a de-interlaced frame.
          


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/af4bf46a-fae7-4485-b5fb-3fd1857f383f">VMR9VideoDesc</a>



<a href="https://msdn.microsoft.com/e2da0c1e-d592-49ce-937c-0d75ce270282">VMR9VideoStreamInfo</a>
 

 


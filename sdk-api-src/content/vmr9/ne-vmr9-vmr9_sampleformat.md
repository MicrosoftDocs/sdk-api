---
UID: NE:vmr9._VMR9_SampleFormat
title: VMR9_SampleFormat (vmr9.h)
description: The VMR9_SampleFormat enumeration type describes the interlacing of a video stream.
helpviewer_keywords: ["VMR9_SampleFieldInterleavedEvenFirst","VMR9_SampleFieldInterleavedOddFirst","VMR9_SampleFieldSingleEven","VMR9_SampleFieldSingleOdd","VMR9_SampleFormat","VMR9_SampleFormat","VMR9_SampleFormat enumeration [DirectShow]","VMR9_SampleProgressiveFrame","VMR9_SampleReserved","dshow.vmr9_sampleformat","vmr9/VMR9_SampleFieldInterleavedEvenFirst","vmr9/VMR9_SampleFieldInterleavedOddFirst","vmr9/VMR9_SampleFieldSingleEven","vmr9/VMR9_SampleFieldSingleOdd","vmr9/VMR9_SampleFormat","vmr9/VMR9_SampleProgressiveFrame","vmr9/VMR9_SampleReserved"]
old-location: dshow\vmr9_sampleformat.htm
tech.root: dshow
ms.assetid: 0e501c05-91ac-4594-bdfe-e8b4bfeb5bcb
ms.date: 12/05/2018
ms.keywords: VMR9_SampleFieldInterleavedEvenFirst, VMR9_SampleFieldInterleavedOddFirst, VMR9_SampleFieldSingleEven, VMR9_SampleFieldSingleOdd, VMR9_SampleFormat, VMR9_SampleFormat , VMR9_SampleFormat enumeration [DirectShow], VMR9_SampleProgressiveFrame, VMR9_SampleReserved, dshow.vmr9_sampleformat, vmr9/VMR9_SampleFieldInterleavedEvenFirst, vmr9/VMR9_SampleFieldInterleavedOddFirst, vmr9/VMR9_SampleFieldSingleEven, vmr9/VMR9_SampleFieldSingleOdd, vmr9/VMR9_SampleFormat, vmr9/VMR9_SampleProgressiveFrame, vmr9/VMR9_SampleReserved
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
targetos: Windows
req.typenames: VMR9_SampleFormat
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VMR9_SampleFormat
 - vmr9/_VMR9_SampleFormat
 - VMR9_SampleFormat
 - vmr9/VMR9_SampleFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmr9.h
api_name:
 - VMR9_SampleFormat
---

# VMR9_SampleFormat enumeration


## -description

The <b>VMR9_SampleFormat</b> enumeration type describes the interlacing of a video stream.

## -enum-fields

### -field VMR9_SampleReserved:1

Reserved; do not use.

### -field VMR9_SampleProgressiveFrame:2

Progressive frame; no interleaving

### -field VMR9_SampleFieldInterleavedEvenFirst:3

Each sample contains two interleaved fields, with the even field first.

### -field VMR9_SampleFieldInterleavedOddFirst:4

Each sample contains two interleaved fields, with the odd field first.

### -field VMR9_SampleFieldSingleEven:5

The sample contains a single field, and each line in the sample corresponds to the even lines in a deinterlaced frame. That is, lines 0, 1, 2,... in the sample correspond to lines 0, 2, 4,... in the deinterlaced frame. The missing lines must be constructed when the frame is deinterlaced.

### -field VMR9_SampleFieldSingleOdd:6

The sample contains a single field, and each line in the sample corresponds to the odd lines in a de-interlaced frame.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9videodesc">VMR9VideoDesc</a>



<a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9videostreaminfo">VMR9VideoStreamInfo</a>

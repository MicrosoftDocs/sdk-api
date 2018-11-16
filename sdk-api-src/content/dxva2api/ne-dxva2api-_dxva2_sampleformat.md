---
UID: NE:dxva2api._DXVA2_SampleFormat
title: "_DXVA2_SampleFormat"
author: windows-sdk-content
description: Describes the content of a video sample. These flags are used in the DXVA2_ExtendedFormat structure.
old-location: mf\dxva2_sampleformat.htm
tech.root: medfound
ms.assetid: 7d2d38c0-249d-47c3-acda-ba1bec721a5c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 7d2d38c0-249d-47c3-acda-ba1bec721a5c, DXVA2_SampleFieldInterleavedEvenFirst, DXVA2_SampleFieldInterleavedOddFirst, DXVA2_SampleFieldSingleEven, DXVA2_SampleFieldSingleOdd, DXVA2_SampleFormat, DXVA2_SampleFormat enumeration [Media Foundation], DXVA2_SampleFormatMask, DXVA2_SampleProgressiveFrame, DXVA2_SampleSubStream, DXVA2_SampleUnknown, _DXVA2_SampleFormat, dxva2api/DXVA2_SampleFieldInterleavedEvenFirst, dxva2api/DXVA2_SampleFieldInterleavedOddFirst, dxva2api/DXVA2_SampleFieldSingleEven, dxva2api/DXVA2_SampleFieldSingleOdd, dxva2api/DXVA2_SampleFormat, dxva2api/DXVA2_SampleFormatMask, dxva2api/DXVA2_SampleProgressiveFrame, dxva2api/DXVA2_SampleSubStream, dxva2api/DXVA2_SampleUnknown, mf.dxva2_sampleformat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - dxva2api.h
api_name:
 - DXVA2_SampleFormat
product: Windows
targetos: Windows
req.typenames: DXVA2_SampleFormat
req.redist: 
---

# _DXVA2_SampleFormat enumeration


## -description



Describes the content of a video sample. These flags are used in the <a href="https://msdn.microsoft.com/eba2c56b-8951-4dc5-91ae-1371793ce787">DXVA2_ExtendedFormat</a> structure.




## -enum-fields




### -field DXVA2_SampleFormatMask

Bitmask to validate flag values. This value is not a valid flag.


### -field DXVA2_SampleUnknown

Unknown format. Default to DXVA2_SampleProgressiveFrame.


### -field DXVA2_SampleProgressiveFrame

The sample contains a progressive (non-interlaced) frame.


### -field DXVA2_SampleFieldInterleavedEvenFirst

The sample contains two interleaved fields. The even field should be displayed first.


### -field DXVA2_SampleFieldInterleavedOddFirst

The sample contains two interleaved fields. The odd field should be displayed first.


### -field DXVA2_SampleFieldSingleEven

The sample contains a single even field.


### -field DXVA2_SampleFieldSingleOdd

The sample contains a single odd field.


### -field DXVA2_SampleSubStream

The sample contains a video substream frame. Use this value for substream mixing.


## -remarks



This enumeration is equivalent to the <b>DXVA_SampleFormat</b> enumeration used in DXVA 1.0.

The following table shows the mapping from <a href="https://msdn.microsoft.com/10a3d7b1-74ed-46cd-b10e-59a8f01726d5">MFVideoInterlaceMode</a> enumeration values, which are used in Media Foundation media types, to <b>DXVA2_SampleFormat</b> values.

<table>
<tr>
<th>MFVideoInterlaceMode Value</th>
<th>DXVA2_SampleFormat Value</th>
</tr>
<tr>
<td>MFVideoInterlace_Unknown</td>
<td>DXVA2_SampleUnknown.</td>
</tr>
<tr>
<td>MFVideoInterlace_Progressive</td>
<td>DXVA2_SampleProgressiveFrame.</td>
</tr>
<tr>
<td>MFVideoInterlace_FieldInterleavedUpperFirst</td>
<td>DXVA2_SampleFieldInterleavedEvenFirst</td>
</tr>
<tr>
<td>MFVideoInterlace_FieldInterleavedLowerFirst</td>
<td>DXVA2_SampleFieldInterleavedOddFirst.</td>
</tr>
<tr>
<td>MFVideoInterlace_FieldSingleUpper</td>
<td>DXVA2_SampleFieldSingleEven.</td>
</tr>
<tr>
<td>MFVideoInterlace_FieldSingleLower</td>
<td>DXVA2_SampleFieldSingleOdd.</td>
</tr>
<tr>
<td>MFVideoInterlace_MixedInterlaceOrProgressive</td>
<td>No exact match. Use DXVA2_SampleFieldInterleavedEvenFirst as an initial value, then use the interlace flags from the media samples. For more information, see <a href="https://msdn.microsoft.com/2911ae57-1703-4a9d-bd33-94af1e0f8804">Video Interlacing</a>.</td>
</tr>
</table>
 

With the exception of MFVideoInterlace_MixedInterlaceOrProgressive, each pair of corresponding enumeration values has the same numeric value.

The value DXVA2_SampleSubStream has no equivalent in the <a href="https://msdn.microsoft.com/10a3d7b1-74ed-46cd-b10e-59a8f01726d5">MFVideoInterlaceMode</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 


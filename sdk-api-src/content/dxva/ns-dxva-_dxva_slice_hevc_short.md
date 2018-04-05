---
UID: NS:dxva._DXVA_Slice_HEVC_Short
title: "_DXVA_Slice_HEVC_Short"
author: windows-driver-content
description: Specifies slice control data.
old-location: mf\dxva_slice_hevc_short.htm
old-project: medfound
ms.assetid: ae3399e9-b78c-473d-8ed5-e570dfb676aa
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*LPDXVA_Slice_HEVC_Short, DXVA_Slice_HEVC_Short, DXVA_Slice_HEVC_Short structure [Media Foundation], LPDXVA_Slice_HEVC_Short, LPDXVA_Slice_HEVC_Short structure pointer [Media Foundation], _DXVA_Slice_HEVC_Short, dxva/DXVA_Slice_HEVC_Short, dxva/LPDXVA_Slice_HEVC_Short, mf.dxva_slice_hevc_short"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dxva.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DXVA_Slice_HEVC_Short, *LPDXVA_Slice_HEVC_Short
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxva.h
api_name:
-	DXVA_Slice_HEVC_Short
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVA_Slice_HEVC_Short structure


## -description


 Specifies slice control data. 


## -struct-fields




### -field BSNALunitDataLocation

Specifies the location of the NAL unit. 


### -field SliceBytesInBuffer

The number of bytes in the bitstream data buffer that are associated with this slice control data structure.


### -field wBadSliceChopping

If off-host bitstream parsing is used, this value indicates the bad slice chopping and contains one of the following values:


<table>
<tr>
<td>Value</td>
<td>Description</td>
</tr>
<tr>
<td>0</td>
<td>All bits for the slice are located within the corresponding bitstream data buffer. </td>
</tr>
<tr>
<td>1</td>
<td>The bitstream data buffer contains the start of the slice, but not the entire slice, because the buffer is full. </td>
</tr>
<tr>
<td>2</td>
<td>The bitstream data buffer contains the end of the slice. It does not contain the start of the slice, because the start of the slice was located in the previous bitstream data buffer. </td>
</tr>
<tr>
<td>3</td>
<td>The bitstream data buffer does not contain the start of the slice  because the start of the slice was located in the previous bitstream data buffer and it does not contain the end of the slice becuase the current bitstream data buffer is also full. </td>
</tr>
</table>
 




## -remarks



<b>DXVA_Slice_HEVC_Short</b>   contains slice control data which is passed to the hardware accelerator from the host software decoder. 




## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 


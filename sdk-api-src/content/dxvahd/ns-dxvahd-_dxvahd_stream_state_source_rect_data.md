---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_SOURCE_RECT_DATA
title: "_DXVAHD_STREAM_STATE_SOURCE_RECT_DATA"
author: windows-sdk-content
description: Specifies the source rectangle for an input stream when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
old-location: mf\dxvahd_stream_state_source_rect_data.htm
tech.root: medfound
ms.assetid: 51f2cfe6-722b-4273-abf6-e1b8fdec9808
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: DXVAHD_STREAM_STATE_SOURCE_RECT_DATA, DXVAHD_STREAM_STATE_SOURCE_RECT_DATA structure [Media Foundation], FALSE, TRUE, _DXVAHD_STREAM_STATE_SOURCE_RECT_DATA, dxvahd/DXVAHD_STREAM_STATE_SOURCE_RECT_DATA, mf.dxvahd_stream_state_source_rect_data
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - dxvahd.h
api_name:
 - DXVAHD_STREAM_STATE_SOURCE_RECT_DATA
product: Windows
targetos: Windows
req.typenames: DXVAHD_STREAM_STATE_SOURCE_RECT_DATA
req.redist: 
---

# _DXVAHD_STREAM_STATE_SOURCE_RECT_DATA structure


## -description


Specifies the source rectangle for an input stream when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD)


## -struct-fields




### -field Enable

<b></b>Specifies whether to blit the entire input surface or just the source rectangle. The default state value is <b>FALSE</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Use the source rectangle specified in the <b>SourceRect</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Blit the entire input surface. Ignore the <b>SourceRect</b> member.

</td>
</tr>
</table>
 


### -field SourceRect

The <i>source rectangle</i>, which defines the portion of the input sample that is blitted to the destination surface. The source rectangle is given in pixel coordinates, relative to the input surface. The default state value is an empty rectangle, (0, 0, 0, 0).

If the <b>Enable</b> member is <b>FALSE</b>, the <b>SourceRect</b> member is ignored.


## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/75036101-7498-4d66-afc3-df76ae3cca39">DXVAHD_STREAM_STATE</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/40a8444f-576e-40ff-804e-0912812f0ee6">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 


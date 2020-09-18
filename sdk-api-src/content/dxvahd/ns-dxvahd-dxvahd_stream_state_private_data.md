---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_PRIVATE_DATA
title: DXVAHD_STREAM_STATE_PRIVATE_DATA (dxvahd.h)
description: Contains data for a private stream state, for a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) input stream.
helpviewer_keywords: ["DXVAHD_STREAM_STATE_PRIVATE_DATA","DXVAHD_STREAM_STATE_PRIVATE_DATA structure [Media Foundation]","DXVAHD_STREAM_STATE_PRIVATE_IVTC","dxvahd/DXVAHD_STREAM_STATE_PRIVATE_DATA","mf.dxvahd_stream_state_private_data"]
old-location: mf\dxvahd_stream_state_private_data.htm
tech.root: mf
ms.assetid: 3b7ce487-edec-4ff2-b971-72ddcc28162c
ms.date: 12/05/2018
ms.keywords: DXVAHD_STREAM_STATE_PRIVATE_DATA, DXVAHD_STREAM_STATE_PRIVATE_DATA structure [Media Foundation], DXVAHD_STREAM_STATE_PRIVATE_IVTC, dxvahd/DXVAHD_STREAM_STATE_PRIVATE_DATA, mf.dxvahd_stream_state_private_data
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
targetos: Windows
req.typenames: DXVAHD_STREAM_STATE_PRIVATE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_STREAM_STATE_PRIVATE_DATA
 - dxvahd/_DXVAHD_STREAM_STATE_PRIVATE_DATA
 - DXVAHD_STREAM_STATE_PRIVATE_DATA
 - dxvahd/DXVAHD_STREAM_STATE_PRIVATE_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_STREAM_STATE_PRIVATE_DATA
---

# DXVAHD_STREAM_STATE_PRIVATE_DATA structure


## -description

Contains data for a private stream state, for  a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) input stream.

## -struct-fields

### -field Guid

A GUID that identifies the private stream state. The following GUID is defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DXVAHD_STREAM_STATE_PRIVATE_IVTC"></a><a id="dxvahd_stream_state_private_ivtc"></a><dl>
<dt><b>DXVAHD_STREAM_STATE_PRIVATE_IVTC</b></dt>
</dl>
</td>
<td width="60%">
Retrieves statistics about inverse telecine. The state data (<b>pData</b>) is a <a href="/windows/win32/api/dxvahd/ns-dxvahd-dxvahd_stream_state_private_ivtc_data">DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA</a> structure.

</td>
</tr>
</table>
 

A device can define additional GUIDs for use with custom stream states. The interpretation of the data is then defined by the device.

### -field DataSize

The size, in bytes, of the buffer pointed to by the <b>pData</b> member.

### -field pData

A pointer to a buffer that contains the private state data. The DXVA-HD runtime passes this buffer directly to the device, without validation.

## -remarks

Use this structure for proprietary or device-specific state parameters.

The caller allocates the <b>pData</b> array. Set the <b>DataSize</b> member to the size of the array in bytes. When retrieving the state data, you can set the <b>pData</b> member to <b>NULL</b> to get the size of the data. The device will return the size in the <b>DataSize</b> member.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_stream_state">DXVAHD_STREAM_STATE</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>
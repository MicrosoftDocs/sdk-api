---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA
title: DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA (dxvahd.h)
description: Contains inverse telecine (IVTC) statistics from a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
helpviewer_keywords: ["DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA","DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA structure [Media Foundation]","dxvahd/DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA","mf.dxvahd_stream_state_private_ivtc_data"]
old-location: mf\dxvahd_stream_state_private_ivtc_data.htm
tech.root: mf
ms.assetid: 166fc57e-3b49-44c1-8c6c-691950e7b675
ms.date: 12/05/2018
ms.keywords: DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA, DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA structure [Media Foundation], dxvahd/DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA, mf.dxvahd_stream_state_private_ivtc_data
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
req.typenames: DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA
 - dxvahd/_DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA
 - DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA
 - dxvahd/DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA
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
 - DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA
---

# DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA structure


## -description

Contains inverse telecine (IVTC) statistics from a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

## -struct-fields

### -field Enable

Specifies whether IVTC statistics are enabled. The default state value is <b>FALSE</b>. Setting the value to <b>TRUE</b> enables IVTC statistics, and resets all of the IVTC statistical data to zero.

### -field ITelecineFlags

If the driver detects that the frames are telecined, and is able to perform inverse telecine, this field contains a member of the <a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_itelecine_caps">DXVAHD_ITELECINE_CAPS</a> enumeration. Otherwise, the value is 0.

### -field Frames

The number of consecutive telecined frames that the device has detected.

### -field InputField

The index of the most recent input field. The value  of this member equals the most recent value of the <b>InputFrameOrField</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_stream_data">DXVAHD_STREAM_DATA</a> structure.

## -remarks

If the DXVA-HD device supports IVTC statistics, it can detect when the input video contains telecined frames. You can use this information to enable IVTC in the device.

To enable IVTC statistics, do the following:

<ol>
<li>Allocate a <b>DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA</b> structure and set the <b>Enable</b> member to <b>TRUE</b>.</li>
<li>Initialize a <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_stream_state_private_data">DXVAHD_STREAM_STATE_PRIVATE_DATA</a> structure with these values:<ul>
<li>Set <b>Guid</b>  to <b>DXVAHD_STREAM_STATE_PRIVATE_IVTC</b>.</li>
<li>Set <b>DataSize</b> to <code>sizeof(DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA)</code>.</li>
<li>Set <b>pData</b>  to point to the <b>DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA</b> structure.</li>
</ul>
</li>
<li>Call the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a> method. Set the <i>State</i> parameter of that method to <b>DXVAHD_STREAM_STATE_PRIVATE</b> and the <i>pData</i>  parameter to the address of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_stream_state_private_data">DXVAHD_STREAM_STATE_PRIVATE_DATA</a> structure.</li>
</ol>
To get the most recent IVTC statistics from the device, call the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-getvideoprocessstreamstate">IDXVAHD_VideoProcessor::GetVideoProcessStreamState</a> method. The state parameter and data buffer are the same.

Typically, an application would use this feature as follows:

<ol>
<li>Enable IVTC statistics.</li>
<li>Begin sending interlaced video frames to the DXVA-HD device.</li>
<li>At some point, query the device for the current IVTC statistics.</li>
<li>If the device detects telecined frames, use a custom frame rate to perform IVTC. For more information, see <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_custom_rate_data">DXVAHD_CUSTOM_RATE_DATA</a>.</li>
</ol>

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ne-dxvahd-dxvahd_stream_state">DXVAHD_STREAM_STATE</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>
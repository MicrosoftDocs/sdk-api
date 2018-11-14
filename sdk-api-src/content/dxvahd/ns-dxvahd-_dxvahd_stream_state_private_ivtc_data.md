---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA
title: "_DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA"
author: windows-sdk-content
description: Contains inverse telecine (IVTC) statistics from a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\dxvahd_stream_state_private_ivtc_data.htm
tech.root: medfound
ms.assetid: 166fc57e-3b49-44c1-8c6c-691950e7b675
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA, DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA structure [Media Foundation], _DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA, dxvahd/DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA, mf.dxvahd_stream_state_private_ivtc_data
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA
product: Windows
targetos: Windows
req.typenames: DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA
req.redist: 
---

# _DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA structure


## -description


Contains inverse telecine (IVTC) statistics from a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -struct-fields




### -field Enable

Specifies whether IVTC statistics are enabled. The default state value is <b>FALSE</b>. Setting the value to <b>TRUE</b> enables IVTC statistics, and resets all of the IVTC statistical data to zero.


### -field ITelecineFlags

If the driver detects that the frames are telecined, and is able to perform inverse telecine, this field contains a member of the <a href="https://msdn.microsoft.com/bf3e0d24-2671-4e79-9cfe-d776d8e5fb47">DXVAHD_ITELECINE_CAPS</a> enumeration. Otherwise, the value is 0.


### -field Frames

The number of consecutive telecined frames that the device has detected.


### -field InputField

The index of the most recent input field. The value  of this member equals the most recent value of the <b>InputFrameOrField</b> member of the <a href="https://msdn.microsoft.com/95d74c87-5884-4004-926f-108e9bbb012d">DXVAHD_STREAM_DATA</a> structure.


## -remarks



If the DXVA-HD device supports IVTC statistics, it can detect when the input video contains telecined frames. You can use this information to enable IVTC in the device.

To enable IVTC statistics, do the following:

<ol>
<li>Allocate a <b>DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA</b> structure and set the <b>Enable</b> member to <b>TRUE</b>.</li>
<li>Initialize a <a href="https://msdn.microsoft.com/3b7ce487-edec-4ff2-b971-72ddcc28162c">DXVAHD_STREAM_STATE_PRIVATE_DATA</a> structure with these values:<ul>
<li>Set <b>Guid</b>  to <b>DXVAHD_STREAM_STATE_PRIVATE_IVTC</b>.</li>
<li>Set <b>DataSize</b> to <code>sizeof(DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA)</code>.</li>
<li>Set <b>pData</b>  to point to the <b>DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA</b> structure.</li>
</ul>
</li>
<li>Call the <a href="https://msdn.microsoft.com/40a8444f-576e-40ff-804e-0912812f0ee6">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a> method. Set the <i>State</i> parameter of that method to <b>DXVAHD_STREAM_STATE_PRIVATE</b> and the <i>pData</i>  parameter to the address of the <a href="https://msdn.microsoft.com/3b7ce487-edec-4ff2-b971-72ddcc28162c">DXVAHD_STREAM_STATE_PRIVATE_DATA</a> structure.</li>
</ol>
To get the most recent IVTC statistics from the device, call the <a href="https://msdn.microsoft.com/1ceeae95-d67d-4f11-b815-f4eef517e7ce">IDXVAHD_VideoProcessor::GetVideoProcessStreamState</a> method. The state parameter and data buffer are the same.

Typically, an application would use this feature as follows:

<ol>
<li>Enable IVTC statistics.</li>
<li>Begin sending interlaced video frames to the DXVA-HD device.</li>
<li>At some point, query the device for the current IVTC statistics.</li>
<li>If the device detects telecined frames, use a custom frame rate to perform IVTC. For more information, see <a href="https://msdn.microsoft.com/12cac4a8-cfdf-484c-8443-ef47dd3a152b">DXVAHD_CUSTOM_RATE_DATA</a>.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/75036101-7498-4d66-afc3-df76ae3cca39">DXVAHD_STREAM_STATE</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/40a8444f-576e-40ff-804e-0912812f0ee6">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 


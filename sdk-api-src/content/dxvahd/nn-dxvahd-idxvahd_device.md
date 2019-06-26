---
UID: NN:dxvahd.IDXVAHD_Device
title: IDXVAHD_Device (dxvahd.h)
author: windows-sdk-content
description: Represents a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\idxvahd_device.htm
tech.root: medfound
ms.assetid: 3f79ac9c-2aed-4e1c-bf6f-02f9c54d59cd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXVAHD_Device, IDXVAHD_Device interface [Media Foundation], IDXVAHD_Device interface [Media Foundation],described, dxvahd/IDXVAHD_Device, mf.idxvahd_device
ms.topic: interface
f1_keywords: 
 - "dxvahd/IDXVAHD_Device"
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
 - COM
api_location:
 - dxvahd.h
api_name:
 - IDXVAHD_Device
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXVAHD_Device interface


## -description


Represents a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

To get a pointer to this interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice">DXVAHD_CreateDevice</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXVAHD_Device</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDXVAHD_Device</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXVAHD_Device</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor">CreateVideoProcessor</a>
</td>
<td align="left" width="63%">
Creates a DXVA-HD video processor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface">CreateVideoSurface</a>
</td>
<td align="left" width="63%">
Creates one or more Microsoft Direct3D video surfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorcaps">GetVideoProcessorCaps</a>
</td>
<td align="left" width="63%">
Gets the capabilities of one or more DXVA-HD video processors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorcustomrates">GetVideoProcessorCustomRates</a>
</td>
<td align="left" width="63%">
Gets a list of custom rates that a DXVA-HD video process supports. Custom rates are used for frame-rate conversion and inverse telecine (IVTC).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">GetVideoProcessorDeviceCaps</a>
</td>
<td align="left" width="63%">
Gets the capabilities of the DXVA-HD device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorfilterrange">GetVideoProcessorFilterRange</a>
</td>
<td align="left" width="63%">
Gets the range of values for an image filter that the DXVA-HD device supports.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats">GetVideoProcessorInputFormats</a>
</td>
<td align="left" width="63%">
Gets a list of the input formats supported by the DXVA-HD device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats">GetVideoProcessorOutputFormats</a>
</td>
<td align="left" width="63%">
Gets a list of the input formats supported by the DXVA-HD device.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-video-interfaces">Direct3D Video Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 


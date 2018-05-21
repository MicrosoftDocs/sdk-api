---
UID: NN:dxva2api.IDirectXVideoProcessor
title: IDirectXVideoProcessor
author: windows-driver-content
description: Represents a DirectX Video Acceleration (DXVA) video processor device.
old-location: mf\idirectxvideoprocessor.htm
old-project: medfound
ms.assetid: a9bc3162-4f37-4f0b-8a8e-8ebeb8f0d8d5
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: IDirectXVideoProcessor, IDirectXVideoProcessor interface [Media Foundation], IDirectXVideoProcessor interface [Media Foundation],described, a9bc3162-4f37-4f0b-8a8e-8ebeb8f0d8d5, dxva2api/IDirectXVideoProcessor, mf.idirectxvideoprocessor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: DXVA2_SurfaceType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxva2api.h
api_name:
-	IDirectXVideoProcessor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDirectXVideoProcessor interface


## -description


Represents a DirectX Video Acceleration (DXVA) video processor device. To get a pointer to this interface, call <a href="https://msdn.microsoft.com/18178a10-f902-4d25-992e-a27145204321">IDirectXVideoProcessorService::CreateVideoProcessor</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectXVideoProcessor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectXVideoProcessor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectXVideoProcessor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9ea3311-8642-4651-b9da-fbba08ec92fb">GetCreationParameters</a>
</td>
<td align="left" width="63%">
Retrieves the parameters that were used to create this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/550c426b-a194-4ed6-9a90-b79a93e79322">GetFilterPropertyRange</a>
</td>
<td align="left" width="63%">
Retrieves the range of values for an image filter supported by this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e15c8425-7a0b-4d03-b2da-467c800c57c2">GetProcAmpRange</a>
</td>
<td align="left" width="63%">
Retrieves the range of values for a video processor (ProcAmp) setting on this video processor device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451674">GetVideoProcessorCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the video processor device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/920bc584-16ea-4f66-b507-2fe63bfd4fd5">GetVideoProcessorService</a>
</td>
<td align="left" width="63%">
Retrieves the DXVA video processor service that created this video processor device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a199ad3-621e-4594-a9f8-ad6cfd560cec">VideoProcessBlt</a>
</td>
<td align="left" width="63%">
Performs a video process operation on one or more input samples and writes the result to a Direct3D9 surface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bd688f81-4b7c-4016-b0bd-e40782131f8e">DXVA Video Processing</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 


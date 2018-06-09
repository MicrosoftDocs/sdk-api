---
UID: NN:dxvahd.IDXVAHD_VideoProcessor
title: IDXVAHD_VideoProcessor
author: windows-sdk-content
description: Represents a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
old-location: mf\idxvahd_videoprocessor.htm
old-project: medfound
ms.assetid: cbfacff5-1cbb-4296-8242-c06b43fc95af
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IDXVAHD_VideoProcessor, IDXVAHD_VideoProcessor interface [Media Foundation], IDXVAHD_VideoProcessor interface [Media Foundation],described, dxvahd/IDXVAHD_VideoProcessor, mf.idxvahd_videoprocessor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DXVAHD_SURFACE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxvahd.h
api_name:
 - IDXVAHD_VideoProcessor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXVAHD_VideoProcessor interface


## -description


Represents a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor. 

To get a pointer to this interface, call the <a href="https://msdn.microsoft.com/903e2c05-e4d4-42ca-a28d-6d4738ae6cfc">IDXVAHD_Device::CreateVideoProcessor</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXVAHD_VideoProcessor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDXVAHD_VideoProcessor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXVAHD_VideoProcessor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fdb0d39-7a64-41fd-8f70-4085ddbc7ebc">GetVideoProcessBltState</a>
</td>
<td align="left" width="63%">
Gets the value of a state parameter for a DXVA-HD blit operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ceeae95-d67d-4f11-b815-f4eef517e7ce">GetVideoProcessStreamState</a>
</td>
<td align="left" width="63%">
Gets the value of a state parameter for a DXVA-HD input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adc08662-7977-402d-9eb1-505333550fc8">SetVideoProcessBltState</a>
</td>
<td align="left" width="63%">
Sets a state parameter for a DXVA-HD blit operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40a8444f-576e-40ff-804e-0912812f0ee6">SetVideoProcessStreamState</a>
</td>
<td align="left" width="63%">
Sets a state parameter for a DXVA-HD input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59c4deee-4ef2-4aba-8188-989904055e70">VideoProcessBltHD</a>
</td>
<td align="left" width="63%">
Performs a video processing blit on one or more input samples and writes the result to a Microsoft Direct3D surface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/adddf378-f71c-4f81-bcf1-5d729a03eb58">Direct3D Video Interfaces</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 


---
UID: NN:dxgi1_3.IDXGISwapChainMedia
title: IDXGISwapChainMedia
author: windows-sdk-content
description: This swap chain interface allows desktop media applications to request a seamless change to a specific refresh rate.
old-location: direct3ddxgi\idxgiswapchainmedia.htm
old-project: direct3ddxgi
ms.assetid: 80C2A6D8-3435-4671-A473-0EF0F5A70ADB
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDXGISwapChainMedia, IDXGISwapChainMedia interface [DXGI], IDXGISwapChainMedia interface [DXGI],described, direct3ddxgi.idxgiswapchainmedia, dxgi1_3/IDXGISwapChainMedia
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dxgi1_3.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DXGI_OVERLAY_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGISwapChainMedia
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISwapChainMedia interface


## -description


This swap chain interface allows desktop media applications to request a seamless change to a specific refresh rate.

For example, a media application presenting video at a typical framerate of 23.997 frames per second can request a custom refresh rate of 24 or 48 Hz to eliminate jitter. If the request is approved, the app starts presenting frames at the custom refresh rate immediately - without the typical 'mode switch' a user would experience when changing the refresh rate themselves by using the control panel.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGISwapChainMedia</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDXGISwapChainMedia</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGISwapChainMedia</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3334E761-745E-4476-9AB4-4FC6DABC78E8">CheckPresentDurationSupport</a>
</td>
<td align="left" width="63%">
Queries the graphics driver for a supported frame present duration corresponding to a custom refresh rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AC29C389-832A-4A73-A5D8-7687B1D02256">GetFrameStatisticsMedia</a>
</td>
<td align="left" width="63%">
Queries the system for a  <a href="https://msdn.microsoft.com/BC23B5C1-8257-4556-B930-E09FE60D536C">DXGI_FRAME_STATISTICS_MEDIA</a> structure that indicates whether a custom refresh rate is currently approved by the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F2852200-01B4-4CB7-8635-87CF827E1D27">SetPresentDuration</a>
</td>
<td align="left" width="63%">
Requests a custom presentation duration (custom refresh rate).

</td>
</tr>
</table> 


## -remarks



Seamless changes to custom framerates can only be done on integrated panels. Custom frame rates cannot be applied to external displays. If the DXGI output adapter is attached to an external display then <a href="https://msdn.microsoft.com/3334E761-745E-4476-9AB4-4FC6DABC78E8">CheckPresentDurationSupport</a> will return (0, 0) for upper and lower bounds, indicating that the device does not support seamless refresh rate changes.
        

Custom refresh rates can be used when displaying video with a dynamic framerate. However, the refresh rate change should be kept imperceptible to the user. A best practice for keeping the refresh rate transition imperceptible  is to only set the custom framerate if the app determines it can present at that rate for least 5 seconds.
        




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/5646B34D-EB2C-4161-8FF0-67F96254AFBC">IDXGIFactoryMedia</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 


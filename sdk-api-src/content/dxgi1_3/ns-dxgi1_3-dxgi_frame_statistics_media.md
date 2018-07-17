---
UID: NS:dxgi1_3.DXGI_FRAME_STATISTICS_MEDIA
title: DXGI_FRAME_STATISTICS_MEDIA
author: windows-sdk-content
description: Used to verify system approval for the app's custom present duration (custom refresh rate).
old-location: direct3ddxgi\dxgi_frame_statistics_media.htm
old-project: direct3ddxgi
ms.assetid: BC23B5C1-8257-4556-B930-E09FE60D536C
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: DXGI_FRAME_STATISTICS_MEDIA, DXGI_FRAME_STATISTICS_MEDIA structure [DXGI], direct3ddxgi.dxgi_frame_statistics_media, dxgi1_3/DXGI_FRAME_STATISTICS_MEDIA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: DXGI_FRAME_STATISTICS_MEDIA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_3.h
api_name:
 - DXGI_FRAME_STATISTICS_MEDIA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_FRAME_STATISTICS_MEDIA structure


## -description


Used to verify system approval for the app's custom present duration (custom refresh rate). Approval should be continuously verified on a frame-by-frame basis.


## -struct-fields




### -field PresentCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value that represents the running total count of times that an image was presented to the monitor since the computer booted.

<div class="alert"><b>Note</b>  The number of times that an image was presented to the monitor is not necessarily the same as the number of times 
        that you called <a href="https://msdn.microsoft.com/library/Bb174576(v=VS.85).aspx">IDXGISwapChain::Present</a> or <a href="https://msdn.microsoft.com/F795A719-71BA-4A25-B41A-9D93F96B6CA4">IDXGISwapChain1::Present1</a>.</div>
<div> </div>

### -field PresentRefreshCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value that represents  the running total count of v-blanks at which the last image was presented to the monitor and that have happened since the computer booted (for windowed mode, since the swap chain was created).


### -field SyncRefreshCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value that represents  the running total count of v-blanks when the scheduler last sampled the machine time by calling <a href="https://msdn.microsoft.com/library/ms644904(v=VS.85).aspx">QueryPerformanceCounter</a> and that have happened since the computer booted (for windowed mode, since the swap chain was created).


### -field SyncQPCTime

Type: <b><a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a></b>

A value that represents the high-resolution performance counter timer. 
        This value is the same as the value returned by the <a href="https://msdn.microsoft.com/library/ms644904(v=VS.85).aspx">QueryPerformanceCounter</a> 
        function.


### -field SyncGPUTime

Type: <b><a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a></b>

Reserved. Always returns 0.


### -field CompositionMode

Type: <b><a href="https://msdn.microsoft.com/F9D26722-E8E8-4A2F-A411-D461B96F3F9C">DXGI_FRAME_PRESENTATION_MODE</a></b>

A value indicating the composition presentation mode. This value is used to determine whether the app should continue to use the decode swap chain. See <a href="https://msdn.microsoft.com/F9D26722-E8E8-4A2F-A411-D461B96F3F9C">DXGI_FRAME_PRESENTATION_MODE</a>.


### -field ApprovedPresentDuration

Type: <b>UINT</b>

If the system approves an app's custom present duration request, this field is set to the approved custom present duration.

If the app's custom present duration request is not approved, this field is set to zero.


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/AC29C389-832A-4A73-A5D8-7687B1D02256">GetFrameStatisticsMedia</a> method.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>



<a href="https://msdn.microsoft.com/80C2A6D8-3435-4671-A473-0EF0F5A70ADB">IDXGISwapChainMedia</a>
 

 


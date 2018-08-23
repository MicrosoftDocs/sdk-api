---
UID: NS:dxgi.DXGI_FRAME_STATISTICS
title: DXGI_FRAME_STATISTICS
author: windows-sdk-content
description: Describes timing and presentation statistics for a frame.
old-location: direct3ddxgi\dxgi_frame_statistics.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_frame_statistics.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 97415a25-57a3-0530-e47d-4459bac66c73, DXGI_FRAME_STATISTICS, DXGI_FRAME_STATISTICS structure [DXGI], direct3ddxgi.dxgi_frame_statistics, dxgi/DXGI_FRAME_STATISTICS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxgi.h
req.include-header: 
req.redist: 
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
req.typenames: DXGI_FRAME_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI.h
api_name:
 - DXGI_FRAME_STATISTICS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_FRAME_STATISTICS structure


## -description


Describes timing and presentation statistics for a frame.


## -struct-fields




### -field PresentCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value that represents the running total count of times that an image was presented to the monitor since the computer booted.

<div class="alert"><b>Note</b>  The number of times that an image was presented to the monitor is not necessarily the same as the number of times 
        that you called <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">IDXGISwapChain::Present</a> or <a href="https://msdn.microsoft.com/F795A719-71BA-4A25-B41A-9D93F96B6CA4">IDXGISwapChain1::Present1</a>.</div>
<div> </div>

### -field PresentRefreshCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value that represents  the running total count of v-blanks at which the last image was presented to the monitor and that have happened since the computer booted (for windowed mode, since the swap chain was created).


### -field SyncRefreshCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value that represents  the running total count of v-blanks when the scheduler last sampled the machine time by calling <a href="winmsg.queryperformancecounter">QueryPerformanceCounter</a> and that have happened since the computer booted (for windowed mode, since the swap chain was created).


### -field SyncQPCTime

Type: <b><a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a></b>

A value that represents the high-resolution performance counter timer. 
        This value is the same as the value returned by the <a href="winmsg.queryperformancecounter">QueryPerformanceCounter</a> 
        function.


### -field SyncGPUTime

Type: <b><a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a></b>

Reserved. Always returns 0.


## -remarks



You initialize the <b>DXGI_FRAME_STATISTICS</b> structure with the <a href="https://msdn.microsoft.com/7ce4bf11-b314-4e82-8ad8-4a5e56b6e863">IDXGIOutput::GetFrameStatistics</a> or <a href="https://msdn.microsoft.com/c02b9e3b-5d59-4ed2-b373-2097c0e46f70">IDXGISwapChain::GetFrameStatistics</a> method.

You can only use <a href="https://msdn.microsoft.com/c02b9e3b-5d59-4ed2-b373-2097c0e46f70">IDXGISwapChain::GetFrameStatistics</a> for swap chains that either use the flip presentation model or draw in full-screen mode. You set the <a href="DXGI_SWAP_EFFECT.htm">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> value in the <b>SwapEffect</b> member of the <a href="https://msdn.microsoft.com/38B302DF-5617-4195-8E4A-619D75188AD5">DXGI_SWAP_CHAIN_DESC1</a> structure to specify that the swap chain uses the flip presentation model.

The values in the <b>PresentCount</b> and <b>PresentRefreshCount</b> members indicate information about when a frame was presented on the display screen. You can use these values to determine whether a glitch occurred. The values in the <b>SyncRefreshCount</b> and <b>SyncQPCTime</b> members indicate timing information that you can use for audio and video synchronization or very precise animation. If the swap chain draws in full-screen mode, these values are based on when the computer booted. 
If the swap chain draws in windowed mode, these values are based on when the swap chain is created.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 


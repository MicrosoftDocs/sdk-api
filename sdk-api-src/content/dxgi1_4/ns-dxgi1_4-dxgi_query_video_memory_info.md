---
UID: NS:dxgi1_4.DXGI_QUERY_VIDEO_MEMORY_INFO
title: DXGI_QUERY_VIDEO_MEMORY_INFO
author: windows-sdk-content
description: Describes the current video memory budgeting parameters.
old-location: direct3ddxgi\dxgi_query_video_memory_info.htm
old-project: direct3ddxgi
ms.assetid: E710F3A9-CB12-43B0-B56C-789350BCAE59
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DXGI_QUERY_VIDEO_MEMORY_INFO, DXGI_QUERY_VIDEO_MEMORY_INFO structure [DXGI], direct3ddxgi.dxgi_query_video_memory_info, dxgi1_4/DXGI_QUERY_VIDEO_MEMORY_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxgi1_4.h
req.include-header: DXGI1_3.h
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
req.typenames: DXGI_QUERY_VIDEO_MEMORY_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_4.h
api_name:
 - DXGI_QUERY_VIDEO_MEMORY_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_QUERY_VIDEO_MEMORY_INFO structure


## -description


Describes the current video memory budgeting parameters.


## -struct-fields




### -field Budget

Specifies the OS-provided video memory budget, in bytes, that the application should target. If <i>CurrentUsage</i> is greater than <i>Budget</i>, the application may incur stuttering or performance penalties due to background activity by the OS to provide other applications with a fair usage of video memory.


### -field CurrentUsage

              Specifies the application’s current video memory usage, in bytes.


### -field AvailableForReservation

              The amount of video memory, in bytes, that the application has available for reservation. To reserve this video memory, the application should call <a href="https://msdn.microsoft.com/5D17F57F-9FFA-4B5C-98B6-33E5B3982A63">IDXGIAdapter3::SetVideoMemoryReservation</a>.


### -field CurrentReservation

              The amount of video memory, in bytes, that is reserved by the application. The OS uses the reservation as a hint to determine the application’s minimum working set. Applications should attempt to ensure that their video memory usage can be trimmed to meet this requirement.




## -remarks



Use this structure with <a href="https://msdn.microsoft.com/A2F95FE5-CF8D-4F17-8CC8-62AAA40B71FC">QueryVideoMemoryInfo</a>.

Refer to the remarks for <a href="https://msdn.microsoft.com/EFA3FF00-F121-4ED8-AF83-1952C73AE06D">D3D12_MEMORY_POOL</a>.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 


---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 


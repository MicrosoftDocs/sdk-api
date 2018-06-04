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

# IDXGISwapChainMedia::GetFrameStatisticsMedia


## -description


Queries the system for a  <a href="https://msdn.microsoft.com/BC23B5C1-8257-4556-B930-E09FE60D536C">DXGI_FRAME_STATISTICS_MEDIA</a> structure that indicates whether a custom refresh rate is currently approved by the system.


## -parameters




### -param pStats [out]

A <a href="https://msdn.microsoft.com/BC23B5C1-8257-4556-B930-E09FE60D536C">DXGI_FRAME_STATISTICS_MEDIA</a> structure indicating whether the system currently approves the custom refresh rate request.


## -returns



This method returns S_OK on success, or a DXGI error code on failure.




## -see-also




<a href="https://msdn.microsoft.com/80C2A6D8-3435-4671-A473-0EF0F5A70ADB">IDXGISwapChainMedia</a>
 

 


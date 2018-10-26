---
UID: NF:dxgi1_3.IDXGISwapChainMedia.GetFrameStatisticsMedia
title: IDXGISwapChainMedia::GetFrameStatisticsMedia
author: windows-sdk-content
description: Queries the system for a DXGI_FRAME_STATISTICS_MEDIA structure that indicates whether a custom refresh rate is currently approved by the system.
old-location: direct3ddxgi\idxgiswapchainmedia_getframestatisticsmedia.htm
tech.root: direct3ddxgi
ms.assetid: AC29C389-832A-4A73-A5D8-7687B1D02256
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetFrameStatisticsMedia, GetFrameStatisticsMedia method [DXGI], GetFrameStatisticsMedia method [DXGI],IDXGISwapChainMedia interface, IDXGISwapChainMedia interface [DXGI],GetFrameStatisticsMedia method, IDXGISwapChainMedia.GetFrameStatisticsMedia, IDXGISwapChainMedia::GetFrameStatisticsMedia, direct3ddxgi.idxgiswapchainmedia_getframestatisticsmedia, dxgi1_3/IDXGISwapChainMedia::GetFrameStatisticsMedia
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi1_3.h
req.include-header: 
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
req.lib: Dxgi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGISwapChainMedia.GetFrameStatisticsMedia
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 


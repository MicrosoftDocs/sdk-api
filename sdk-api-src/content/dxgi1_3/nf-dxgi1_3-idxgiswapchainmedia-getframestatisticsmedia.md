---
UID: NF:dxgi1_3.IDXGISwapChainMedia.GetFrameStatisticsMedia
title: IDXGISwapChainMedia::GetFrameStatisticsMedia (dxgi1_3.h)
description: Queries the system for a DXGI_FRAME_STATISTICS_MEDIA structure that indicates whether a custom refresh rate is currently approved by the system.
helpviewer_keywords: ["GetFrameStatisticsMedia","GetFrameStatisticsMedia method [DXGI]","GetFrameStatisticsMedia method [DXGI]","IDXGISwapChainMedia interface","IDXGISwapChainMedia interface [DXGI]","GetFrameStatisticsMedia method","IDXGISwapChainMedia.GetFrameStatisticsMedia","IDXGISwapChainMedia::GetFrameStatisticsMedia","direct3ddxgi.idxgiswapchainmedia_getframestatisticsmedia","dxgi1_3/IDXGISwapChainMedia::GetFrameStatisticsMedia"]
old-location: direct3ddxgi\idxgiswapchainmedia_getframestatisticsmedia.htm
tech.root: direct3ddxgi
ms.assetid: AC29C389-832A-4A73-A5D8-7687B1D02256
ms.date: 12/05/2018
ms.keywords: GetFrameStatisticsMedia, GetFrameStatisticsMedia method [DXGI], GetFrameStatisticsMedia method [DXGI],IDXGISwapChainMedia interface, IDXGISwapChainMedia interface [DXGI],GetFrameStatisticsMedia method, IDXGISwapChainMedia.GetFrameStatisticsMedia, IDXGISwapChainMedia::GetFrameStatisticsMedia, direct3ddxgi.idxgiswapchainmedia_getframestatisticsmedia, dxgi1_3/IDXGISwapChainMedia::GetFrameStatisticsMedia
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGISwapChainMedia::GetFrameStatisticsMedia
 - dxgi1_3/IDXGISwapChainMedia::GetFrameStatisticsMedia
dev_langs:
 - c++
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
---

# IDXGISwapChainMedia::GetFrameStatisticsMedia


## -description

Queries the system for a  <a href="/windows/desktop/api/dxgi1_3/ns-dxgi1_3-dxgi_frame_statistics_media">DXGI_FRAME_STATISTICS_MEDIA</a> structure that indicates whether a custom refresh rate is currently approved by the system.

## -parameters

### -param pStats [out]

A <a href="/windows/desktop/api/dxgi1_3/ns-dxgi1_3-dxgi_frame_statistics_media">DXGI_FRAME_STATISTICS_MEDIA</a> structure indicating whether the system currently approves the custom refresh rate request.

## -returns

This method returns S_OK on success, or a DXGI error code on failure.

## -see-also

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchainmedia">IDXGISwapChainMedia</a>
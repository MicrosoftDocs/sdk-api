---
UID: NF:dxgi1_3.IDXGISwapChainMedia.CheckPresentDurationSupport
title: IDXGISwapChainMedia::CheckPresentDurationSupport
author: windows-driver-content
description: Queries the graphics driver for a supported frame present duration corresponding to a custom refresh rate.
old-location: direct3ddxgi\idxgiswapchainmedia_checkpresentdurationsupport.htm
old-project: direct3ddxgi
ms.assetid: 3334E761-745E-4476-9AB4-4FC6DABC78E8
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: CheckPresentDurationSupport, CheckPresentDurationSupport method [DXGI], CheckPresentDurationSupport method [DXGI],IDXGISwapChainMedia interface, IDXGISwapChainMedia interface [DXGI],CheckPresentDurationSupport method, IDXGISwapChainMedia.CheckPresentDurationSupport, IDXGISwapChainMedia::CheckPresentDurationSupport, direct3ddxgi.idxgiswapchainmedia_checkpresentdurationsupport, dxgi1_3/IDXGISwapChainMedia::CheckPresentDurationSupport
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
req.typenames: DXGI_OVERLAY_SUPPORT_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dxgi.lib
-	Dxgi.dll
api_name:
-	IDXGISwapChainMedia.CheckPresentDurationSupport
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISwapChainMedia::CheckPresentDurationSupport


## -description


Queries the graphics driver for a supported frame present duration corresponding to a custom refresh rate.


## -parameters




### -param DesiredPresentDuration

Indicates the frame duration to check. This value is the duration of one frame at the desired refresh rate, specified in hundreds of nanoseconds. For example, set this field to 167777 to check for 60 Hz refresh rate support.


### -param pClosestSmallerPresentDuration [out]

A variable that will be set to the closest supported frame present duration that's smaller than the requested value, or zero if the device does not support any lower duration.


### -param pClosestLargerPresentDuration [out]

A variable that will be set to the closest supported frame present duration that's larger than the requested value, or zero if the device does not support any higher duration.


## -returns



This method returns S_OK on success, or a DXGI error code on failure.




## -remarks



If the DXGI output adapter does not support custom refresh rates (for example, an external display) then the display driver will set upper and lower bounds to (0, 0).




## -see-also




<a href="https://msdn.microsoft.com/80C2A6D8-3435-4671-A473-0EF0F5A70ADB">IDXGISwapChainMedia</a>
 

 


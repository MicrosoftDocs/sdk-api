---
UID: NE:dxgitype.DXGI_MODE_SCALING
title: DXGI_MODE_SCALING
author: windows-sdk-content
description: Flags indicating how an image is stretched to fit a given monitor's resolution.
old-location: direct3ddxgi\DXGI_MODE_SCALING.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_mode_scaling.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: 5cf7c4a4-7f8e-c9eb-68fb-f347b1e755a0, DXGI_MODE_SCALING, DXGI_MODE_SCALING enumeration [DXGI], DXGI_MODE_SCALING_CENTERED, DXGI_MODE_SCALING_STRETCHED, DXGI_MODE_SCALING_UNSPECIFIED, direct3ddxgi.DXGI_MODE_SCALING, dxgitype/DXGI_MODE_SCALING, dxgitype/DXGI_MODE_SCALING_CENTERED, dxgitype/DXGI_MODE_SCALING_STRETCHED, dxgitype/DXGI_MODE_SCALING_UNSPECIFIED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dxgitype.h
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
req.typenames: DXGI_MODE_SCALING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgitype.h
api_name:
 - DXGI_MODE_SCALING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_MODE_SCALING enumeration


## -description


Flags indicating how an image is stretched to fit a given monitor's resolution.


## -enum-fields




### -field DXGI_MODE_SCALING_UNSPECIFIED

Unspecified scaling.


### -field DXGI_MODE_SCALING_CENTERED

Specifies no scaling. The image is centered on the display. This flag is typically used for a fixed-dot-pitch display (such as an LED display).


### -field DXGI_MODE_SCALING_STRETCHED

Specifies stretched scaling.


## -remarks



Selecting the CENTERED or STRETCHED modes can result in a mode change even if you specify the native resolution of the display in the DXGI_MODE_DESC. If you know the native resolution of the display and want to make sure that you do not initiate a mode change when transitioning a swap chain to full screen (either via ALT+ENTER or <a href="https://msdn.microsoft.com/4762082c-5a61-43a0-b158-a70bbec804d4">IDXGISwapChain::SetFullscreenState</a>), you should use UNSPECIFIED.

This enum is used by the <a href="https://msdn.microsoft.com/8F44CF77-D3A1-44F7-AB7F-69E5727A4378">DXGI_MODE_DESC1</a> and <a href="https://msdn.microsoft.com/0EE5683E-0623-4FD7-A77F-B64F90A25C6A">DXGI_SWAP_CHAIN_FULLSCREEN_DESC</a> structures.




## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 


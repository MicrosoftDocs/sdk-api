---
UID: NE:dxgi1_3.DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS
title: DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS
author: windows-sdk-content
description: Options for swap-chain color space.
old-location: direct3ddxgi\dxgi_multiplane_overlay_ycbcr_flags.htm
tech.root: direct3ddxgi
ms.assetid: 8BD502DC-39C1-472E-AC29-14A1F7EDB37E
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS, DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS enumeration [DXGI], DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_BT709, DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_NOMINAL_RANGE, DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_xvYCC, direct3ddxgi.dxgi_multiplane_overlay_ycbcr_flags, dxgi1_3/DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS, dxgi1_3/DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_BT709, dxgi1_3/DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_NOMINAL_RANGE, dxgi1_3/DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_xvYCC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dxgi1_3.h
req.include-header: DXGIPartner.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_3.h
api_name:
 - DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS
product: Windows
targetos: Windows
req.typenames: DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS
req.redist: 
---

# DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS enumeration


## -description


Options for swap-chain color space.


## -enum-fields




### -field DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_NOMINAL_RANGE

Specifies nominal range YCbCr, which isn't an absolute color space, but a way of encoding RGB info.


### -field DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_BT709

Specifies BT.709, which standardizes the format of high-definition television and has 16:9 (widescreen) aspect ratio.


### -field DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAG_xvYCC

Specifies xvYCC or extended-gamut YCC (also x.v.Color) color space that can be used in the video electronics of television sets to support a gamut 1.8 times as large as that of the sRGB color space.


## -remarks



This enum is used by <a href="https://msdn.microsoft.com/DE0AA2BF-8E98-4CF4-8CC2-760AB4B8776D">SetColorSpace</a>.




## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 


---
UID: NE:d2d1_1.D2D1_BITMAP_OPTIONS
title: D2D1_BITMAP_OPTIONS
author: windows-sdk-content
description: Specifies how a bitmap can be used.
old-location: direct2d\__d2d1_bitmap_options.htm
tech.root: direct2d
ms.assetid: c080e23e-99c4-46ed-8b21-be26dec288af
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: D2D1_BITMAP_OPTIONS, D2D1_BITMAP_OPTIONS enumeration [Direct2D], D2D1_BITMAP_OPTIONS_CANNOT_DRAW, D2D1_BITMAP_OPTIONS_CPU_READ, D2D1_BITMAP_OPTIONS_GDI_COMPATIBLE, D2D1_BITMAP_OPTIONS_NONE, D2D1_BITMAP_OPTIONS_TARGET, d2d1_1/D2D1_BITMAP_OPTIONS, d2d1_1/D2D1_BITMAP_OPTIONS_CANNOT_DRAW, d2d1_1/D2D1_BITMAP_OPTIONS_CPU_READ, d2d1_1/D2D1_BITMAP_OPTIONS_GDI_COMPATIBLE, d2d1_1/D2D1_BITMAP_OPTIONS_NONE, d2d1_1/D2D1_BITMAP_OPTIONS_TARGET, direct2d.__d2d1_bitmap_options
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - D2d1_1.h
api_name:
 - D2D1_BITMAP_OPTIONS
product: Windows
targetos: Windows
req.typenames: D2D1_BITMAP_OPTIONS
req.redist: 
---

# D2D1_BITMAP_OPTIONS enumeration


## -description


Specifies how a bitmap can be used.


## -enum-fields




### -field D2D1_BITMAP_OPTIONS_NONE

The bitmap is created with default properties.


### -field D2D1_BITMAP_OPTIONS_TARGET

The bitmap can be used as a device context target.


### -field D2D1_BITMAP_OPTIONS_CANNOT_DRAW

The bitmap cannot be used as an input. 


### -field D2D1_BITMAP_OPTIONS_CPU_READ

The bitmap can be read from the CPU.


### -field D2D1_BITMAP_OPTIONS_GDI_COMPATIBLE

The bitmap works with <a href="https://msdn.microsoft.com/40797258-84a0-44ee-8b64-04ceb3eb1998">ID2D1GdiInteropRenderTarget::GetDC</a>.

<div class="alert"><b>Note</b>  This flag is not available in Windows Store apps.</div>
<div> </div>

### -field D2D1_BITMAP_OPTIONS_FORCE_DWORD




## -remarks



<b>D2D1_BITMAP_OPTIONS_NONE</b> implies that none of the flags are set. This means that the bitmap can be used for drawing from, cannot be set as a target and cannot be read from by the CPU.

<b>D2D1_BITMAP_OPTIONS_TARGET</b> means that the bitmap can be specified as a target in <a href="https://msdn.microsoft.com/66914048-7bef-4551-bb14-5ab67c727dc5">ID2D1DeviceContext::SetTarget</a>. If you also specify the  <b>D2D1_BITMAP_OPTIONS_CANNOT_DRAW</b> flag the bitmap can be used a target but, it cannot be drawn from. Attempting to draw with a bitmap that has both flags set will result in the device context being put into an error state with <b>D2DERR_BITMAP_CANNOT_DRAW</b>.



<b>D2D1_BITMAP_OPTIONS_CPU_READ</b> means that the bitmap can be mapped by using <a href="https://msdn.microsoft.com/284c16ea-1a9f-4f13-b359-214178650add">ID2D1Bitmap1::Map</a>. This flag requires <b>D2D1_BITMAP_OPTIONS_CANNOT_DRAW</b> and cannot be combined with any other flags. The bitmap must be updated with the <a href="https://msdn.microsoft.com/d43685d9-292c-462c-bdd2-c4e81b6d704e">CopyFromBitmap</a> or <a href="https://msdn.microsoft.com/42e25099-016e-4656-a412-72dd0fbac1fd">CopyFromRenderTarget</a> methods.



<div class="alert"><b>Note</b>  You should only use <b>D2D1_BITMAP_OPTIONS_CANNOT_DRAW</b> is when the purpose of the bitmap is to be a target only or when the bitmap will be mapped .</div>
<div> </div>
<b>D2D1_BITMAP_OPTIONS_GDI_COMPATIBLE</b> means that it is possible to get a DC associated with this bitmap.  This must be used in conjunction with <b>D2D1_BITMAP_OPTIONS_TARGET</b>. The <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a> must be either <b>DXGI_FORMAT_B8G8R8A8_UNORM</b> or <b>DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</b>.




## -see-also




<a href="https://msdn.microsoft.com/8292da6b-8232-4ef0-967d-a53d586aa9a9">ID2D1DeviceContext::CreateBitmap</a>
 

 


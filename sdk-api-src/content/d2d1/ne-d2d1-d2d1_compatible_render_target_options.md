---
UID: NE:d2d1.D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS
title: D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS
author: windows-driver-content
description: Specifies additional features supportable by a compatible render target when it is created. This enumeration allows a bitwise combination of its member values.
old-location: direct2d\D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS.htm
old-project: Direct2D
ms.assetid: c20bf016-2304-4bd3-88ad-42d81e69c302
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS, D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS enumeration [Direct2D], D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_GDI_COMPATIBLE, D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE, d2d1/D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS, d2d1/D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_GDI_COMPATIBLE, d2d1/D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE, direct2d.D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctxtcall.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d2d1.h
api_name:
-	D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS enumeration


## -description


Specifies additional features supportable by a compatible render target when it is created. 
    This enumeration allows a bitwise combination of its member values.


## -enum-fields




### -field D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE

The render target supports no additional features.


### -field D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_GDI_COMPATIBLE

The render target supports interoperability with the Windows Graphics Device Interface  (GDI). 


### -field D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_FORCE_DWORD




## -remarks



Use this enumeration when creating a compatible render target with the <a href="https://msdn.microsoft.com/4a799a7c-0d2f-460f-99f9-24c6cf7c4537">CreateCompatibleRenderTarget</a> method. For more information about compatible render targets, see the <a href="https://msdn.microsoft.com/8a67babd-20c7-47f4-8dd3-8c0320d89ad6">Render Targets Overview</a>. 

The <b>D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_GDI_COMPATIBLE</b> option may only be requested if the parent render target was created with <a href="https://msdn.microsoft.com/12d717c4-5f81-4bbf-a693-042e51913081">D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE</a> (for most render targets) or <b>D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_GDI_COMPATIBLE</b> (for render targets created by the <a href="https://msdn.microsoft.com/4a799a7c-0d2f-460f-99f9-24c6cf7c4537">CreateCompatibleRenderTarget</a> method).




## -see-also




<a href="https://msdn.microsoft.com/4a799a7c-0d2f-460f-99f9-24c6cf7c4537">CreateCompatibleRenderTarget</a>



<a href="https://msdn.microsoft.com/8a67babd-20c7-47f4-8dd3-8c0320d89ad6">Render Targets Overview</a>
 

 


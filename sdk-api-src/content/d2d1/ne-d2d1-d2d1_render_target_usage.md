---
UID: NE:d2d1.D2D1_RENDER_TARGET_USAGE
title: D2D1_RENDER_TARGET_USAGE
author: windows-sdk-content
description: Describes how a render target is remoted and whether it should be GDI-compatible. This enumeration allows a bitwise combination of its member values.
old-location: direct2d\D2D1_RENDER_TARGET_USAGE.htm
old-project: direct2d
ms.assetid: 12d717c4-5f81-4bbf-a693-042e51913081
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D2D1_RENDER_TARGET_USAGE, D2D1_RENDER_TARGET_USAGE enumeration [Direct2D], D2D1_RENDER_TARGET_USAGE_FORCE_BITMAP_REMOTING, D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE, D2D1_RENDER_TARGET_USAGE_NONE, d2d1/D2D1_RENDER_TARGET_USAGE, d2d1/D2D1_RENDER_TARGET_USAGE_FORCE_BITMAP_REMOTING, d2d1/D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE, d2d1/D2D1_RENDER_TARGET_USAGE_NONE, direct2d.D2D1_RENDER_TARGET_USAGE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctxtcall.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D2D1_RENDER_TARGET_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_RENDER_TARGET_USAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D2D1_RENDER_TARGET_USAGE enumeration


## -description


Describes how a render target is remoted and whether it should be GDI-compatible. This enumeration allows a bitwise combination of its member values.


## -enum-fields




### -field D2D1_RENDER_TARGET_USAGE_NONE

The render target attempts to use Direct3D command-stream remoting and uses bitmap remoting if stream remoting fails. The render target is not GDI-compatible.


### -field D2D1_RENDER_TARGET_USAGE_FORCE_BITMAP_REMOTING

The render target renders content locally and sends it to the terminal services client as a bitmap. 


### -field D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE

The render target can be used efficiently with GDI.


### -field D2D1_RENDER_TARGET_USAGE_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/360900bd-1353-4a92-865c-ad34d5e98123">D2D1_RENDER_TARGET_PROPERTIES</a>
 

 


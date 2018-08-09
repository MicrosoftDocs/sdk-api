---
UID: NF:wingdi.PaintRgn
title: PaintRgn function
author: windows-sdk-content
description: The PaintRgn function paints the specified region by using the brush currently selected into the device context.
old-location: gdi\paintrgn.htm
old-project: gdi
ms.assetid: 7656fb67-d865-459e-b379-4f2e44c76fd0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PaintRgn, PaintRgn function [Windows GDI], _win32_PaintRgn, gdi.paintrgn, wingdi/PaintRgn
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - PaintRgn
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PaintRgn function


## -description


The <b>PaintRgn</b> function paints the specified region by using the brush currently selected into the device context.


## -parameters




### -param hdc [in]

Handle to the device context.


### -param hrgn [in]

Handle to the region to be filled. The region's coordinates are presumed to be logical coordinates.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/c4e0eca5-442b-462b-a4f2-0c628b6d3d38">FillRgn</a>



<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>
 

 


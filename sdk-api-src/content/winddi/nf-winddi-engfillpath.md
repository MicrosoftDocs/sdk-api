---
UID: NF:winddi.EngFillPath
title: EngFillPath function (winddi.h)
author: windows-sdk-content
description: The EngFillPath function fills a path.
old-location: display\engfillpath.htm
tech.root: display
ms.assetid: 81c4ae89-391c-482b-b5dc-ef34d41607a1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EngFillPath, EngFillPath function [Display Devices], display.engfillpath, gdifncs_5128f1e3-265b-4570-8504-1782a07268d5.xml, winddi/EngFillPath
ms.topic: function
f1_keywords:
- winddi/EngFillPath
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Win32k.sys
api_name:
- EngFillPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EngFillPath function


## -description


The <b>EngFillPath</b> function fills a path. 


## -parameters




### -param pso

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-_surfobj">SURFOBJ</a> structure that describes the surface on which to draw.


### -param ppo

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a> structure that defines the path to be filled. Use the <b>PATHOBJ_</b><i>Xxx</i> service routines to enumerate the lines, Bezier curves, and other data that make up the path.


### -param pco

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure. Use the <b>CLIPOBJ_</b><i>Xxx</i> service routines to enumerate the <a href="https://docs.microsoft.com/windows-hardware/drivers/">clip region</a> as a set of rectangles.


### -param pbo

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a> structure that defines the pattern and colors with which to fill.


### -param pptlBrushOrg

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/windef/ns-windef-_pointl">POINTL</a> structure defining the brush origin to use to align the brush pattern on the device.


### -param mix [in]

Defines the foreground and background raster operations to use for the brush.


### -param flOptions [in]

Specifies the mode to use when filling the path. This value should be FP_WINDINGMODE or FP_ALTERNATEMODE. All other flags should be ignored. For more information about these modes, see <a href="https://docs.microsoft.com/windows-hardware/drivers/display/path-fill-modes">Path Fill Modes</a>.


## -returns



The return value is <b>TRUE</b> if GDI is able to fill the path. Otherwise, it is <b>FALSE</b>, and an error code is not logged. If an error is encountered, the return value is <b>FALSE</b>, and an error code is logged.




## -remarks



Whenever GDI fills a path on a <a href="https://docs.microsoft.com/windows-hardware/drivers/">device-managed surface</a>, it can call this entry point depending on a comparison of the fill requirements and the following GCAPS bits: GCAPS_BEZIERS, GCAPS_ALTERNATEFILL, and GCAPS_WINDINGFILL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-pathobj">PATHOBJ</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-_surfobj">SURFOBJ</a>
 

 


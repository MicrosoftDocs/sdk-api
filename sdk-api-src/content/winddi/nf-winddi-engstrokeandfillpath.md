---
UID: NF:winddi.EngStrokeAndFillPath
title: EngStrokeAndFillPath function
author: windows-sdk-content
description: The EngStrokeAndFillPath function causes GDI to fill a path and stroke it at the same time.
old-location: display\engstrokeandfillpath.htm
tech.root: display
ms.assetid: a58ce829-aa55-46d6-b6d0-205140a9548c
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: EngStrokeAndFillPath, EngStrokeAndFillPath function [Display Devices], display.engstrokeandfillpath, gdifncs_aad2693d-6a0e-40ab-ad95-aa38e77c7651.xml, winddi/EngStrokeAndFillPath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - EngStrokeAndFillPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngStrokeAndFillPath function


## -description


The <b>EngStrokeAndFillPath</b> function causes GDI to fill a path and stroke it at the same time.


## -parameters




### -param pso

Pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that defines the drawing surface.


### -param ppo

Pointer to a <a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a> structure that defines the path to be filled. The <b>PATHOBJ_</b><i>Xxx</i> service routines are provided to enumerate the lines, Bezier curves, and other data that make up the path.


### -param pco

Pointer to a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure. The <b>CLIPOBJ_</b><i>Xxx</i> service routines are provided to enumerate the <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a> as a set of rectangles.


### -param pxo

Pointer to a <a href="https://msdn.microsoft.com/a18af8fc-880a-4ac3-905a-1d9384c2b8d7">XFORMOBJ</a> structure that is only needed when a geometric wide line is to be drawn and specifies the transform that converts world coordinates to device coordinates. The path is provided in device coordinates but a geometric wide line is actually widened in world coordinates.

The driver can use the <b>XFORMOBJ_</b><i>Xxx</i> service routines to determine the transform.


### -param pboStroke

Pointer to a <a href="https://msdn.microsoft.com/81216bee-d13f-4880-a839-337a247a6c82">BRUSHOBJ</a> structure that describes the brush to use when stroking the path.


### -param plineattrs

Pointer to a <a href="https://msdn.microsoft.com/40fcd6e2-7ed4-433f-ab8b-cc75a305adb9">LINEATTRS</a> structure.


### -param pboFill

Pointer to a BRUSHOBJ structure that describes the brush to use when filling the path.


### -param pptlBrushOrg

Pointer to a <a href="https://msdn.microsoft.com/68cd23d7-7898-4132-abfe-4dda527889b9">POINTL</a> structure that defines the brush origin for both brushes.


### -param mixFill [in]

Defines the foreground and background raster operations to use for the fill brush.


### -param flOptions [in]

Specifies which fill mode to use. This parameter can be FP_WINDINGMODE or FP_ALTERNATEMODE; all other bits should be ignored. For more information about these modes, see <a href="https://msdn.microsoft.com/fa1fb4b9-5ed6-44a2-8a9e-0c1c82f5ea39">Path Fill Modes</a>.


## -returns



The return value is <b>TRUE</b> if GDI fills the path. If the driver should fill the path, the return value is <b>FALSE</b>, and an error code is not logged. If GDI encounters an unexpected error, such as not being able to realize the brush, the return value is DDI_ERROR, and an error code is logged.




## -remarks



The mix mode defines how the incoming pattern should be mixed with the data already on the device surface. The MIX data type consists of two ROP2 values packed into a single ULONG. The low-order byte defines the foreground raster operation; the next byte defines the background raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/81216bee-d13f-4880-a839-337a247a6c82">BRUSHOBJ</a>



<a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/92a04fe5-146d-4839-a854-1ac50705b447">DrvStrokeAndFillPath</a>



<a href="https://msdn.microsoft.com/40fcd6e2-7ed4-433f-ab8b-cc75a305adb9">LINEATTRS</a>



<a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a>



<a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a>



<a href="https://msdn.microsoft.com/a18af8fc-880a-4ac3-905a-1d9384c2b8d7">XFORMOBJ</a>
 

 


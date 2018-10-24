---
UID: NF:winddi.DrvFillPath
title: DrvFillPath function
author: windows-sdk-content
description: The DrvFillPath function is an optional entry point to handle the filling of closed paths.
old-location: display\drvfillpath.htm
tech.root: display
ms.assetid: 6f499d08-d2a1-46d0-b931-e6c16c4e1d3a
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: DrvFillPath, DrvFillPath function [Display Devices], ddifncs_176fcd15-80b2-49da-a11d-a1ed5ca67201.xml, display.drvfillpath, winddi/DrvFillPath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
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
 - winddi.h
api_name:
 - DrvFillPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvFillPath function


## -description


The <b>DrvFillPath</b> function is an optional entry point to handle the filling of closed paths.


## -parameters




### -param pso [in, out]

Pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that defines the surface on which to draw.


### -param ppo [in]

Pointer to a <a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a> structure that defines the path to be filled. The PATHOBJ_<i>Xxx</i> service routines are provided to enumerate the lines, Bezier curves, and other data that make up the path.


### -param pco [in]

Pointer to a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure. The CLIPOBJ_<i>Xxx</i> service routines are provided to enumerate the <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a> as a set of rectangles.


### -param pbo [in]

Pointer to a <a href="https://msdn.microsoft.com/81216bee-d13f-4880-a839-337a247a6c82">BRUSHOBJ</a> structure that defines the pattern and colors used to fill the closed path. This parameter should be dereferenced only if the fill operation specified in <i>mix</i> requires the use of a brush. For example, if <i>mix</i> is set to BLACKNESS, <i>pbo</i> is not defined and should not be dereferenced.


### -param pptlBrushOrg [in]

Pointer to a <a href="https://msdn.microsoft.com/68cd23d7-7898-4132-abfe-4dda527889b9">POINTL</a> structure that defines the brush origin, which is used to align the brush pattern on the device.


### -param mix [in]

The mix mode that defines the foreground and background raster operations to use for the brush. For more information about mix mode, see Remarks. 


### -param flOptions [in]

Specifies either FP_WINDINGMODE, indicating that a winding mode fill should be performed, or FP_ALTERNATEMODE, indicating that an alternating mode fill should be performed. All other flags should be ignored. For more information about these modes, see <a href="https://msdn.microsoft.com/fa1fb4b9-5ed6-44a2-8a9e-0c1c82f5ea39">Path Fill Modes</a>.


## -returns



The return value is <b>TRUE</b> if the driver is able to fill the path. If the path or clipping is too complex to be handled by the driver and should be handled by GDI, the return value is <b>FALSE</b>, and an error code is not logged. If the driver encounters an unexpected error, such as not being able to realize the brush, the return value is DDI_ERROR, and an error code is logged.




## -remarks



GDI can call <b>DrvFillPath</b> to fill a path on a <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device-managed surface</a>. When deciding whether to call this function, GDI compares the fill requirements with the following flags in the <b>flGraphicsCaps</b> member of the <a href="https://msdn.microsoft.com/5ba3e521-2e70-4a5b-979d-30a061275d42">DEVINFO</a> structure: GCAPS_BEZIERS, GCAPS_ALTERNATEFILL, and GCAPS_WINDINGFILL.

The mix mode defines how the incoming pattern should be mixed with the data that is already on the device surface. The MIX data type consists of two binary raster operation (ROP2) values packed into a single ULONG. The lowest-order byte defines the foreground raster operation; the next byte defines the background raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation. 




## -see-also




<a href="https://msdn.microsoft.com/81216bee-d13f-4880-a839-337a247a6c82">BRUSHOBJ</a>



<a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/5ba3e521-2e70-4a5b-979d-30a061275d42">DEVINFO</a>



<a href="https://msdn.microsoft.com/92a04fe5-146d-4839-a854-1ac50705b447">DrvStrokeAndFillPath</a>



<a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a>



<a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a>
 

 


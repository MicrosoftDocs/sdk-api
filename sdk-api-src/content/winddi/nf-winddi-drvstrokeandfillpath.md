---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# DrvStrokeAndFillPath function


## -description


The <b>DrvStrokeAndFillPath</b> function strokes (outlines) and fills a path concurrently.


## -parameters




### -param pso [in, out]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure that describes the surface on which to draw.


### -param ppo [in, out]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a> structure that describes the path to be filled. The PATHOBJ_<i>Xxx</i> service routines are provided to enumerate the lines, Bezier curves, and other data that make up the path.


### -param pco [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a> structure. The CLIPOBJ_<i>Xxx</i> service routines are provided to enumerate the <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a> as a set of rectangles.


### -param pxo [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570618">XFORMOBJ</a> structure that is required when a geometric wide line is drawn. It specifies the transform that takes world coordinates to device coordinates. This is needed because the path is provided in device coordinates but a geometric wide line is actually widened in world coordinates. The XFORMOBJ can be queried to find out what the transform is.


### -param pboStroke [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a> structure that specifies the brush to use when stroking the path.


### -param plineattrs [in]

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568195">LINEATTRS</a> structure that describes the attributes of the line to be drawn.


### -param pboFill [in]

Pointer to a BRUSHOBJ structure that specifies the brush to use when filling the path.


### -param pptlBrushOrg [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that specifies the brush origin for both brushes.


### -param mixFill [in]

The mix mode that defines the foreground and background raster operations to use for the brush. For more information about mix mode, see Remarks. 


### -param flOptions [in]

Specifies either FP_WINDINGMODE, meaning that a winding mode fill should be performed, or FP_ALTERNATEMODE, meaning that an alternating mode fill should be performed. All other flags should be ignored. For more information about these modes, see <a href="https://msdn.microsoft.com/fa1fb4b9-5ed6-44a2-8a9e-0c1c82f5ea39">Path Fill Modes</a>.


## -returns



The return value is <b>TRUE</b> if the driver is able to fill the path. Otherwise, if GDI should instead fill the path, the return value is <b>FALSE</b>. If an error occurs, the return value is DDI_ERROR, and an error code is logged.




## -remarks



If a wide line is used for stroking, the filled area must be reduced to compensate.

The driver can return <b>FALSE</b> if the path or the clipping is too complex for the device to handle; in that case, GDI converts to a simpler call. For example, if the device driver has set the GCAPS_BEZIERS flag in the <b>flGraphicsCaps</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552835">DEVINFO</a> structure and then receives a path with Bezier curves, it can return <b>FALSE</b>; GDI will then convert the Bezier curves to lines and call <b>DrvStrokeAndFillPath</b> again. If the device driver returns <b>FALSE</b> again, GDI will further simplify the call, making calls to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556316">DrvStrokePath</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff556220">DrvFillPath</a>, or to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556180">DrvBitBlt</a>, depending on the mix and width of the lines making up the path.

The mix mode defines how the incoming pattern should be mixed with the data that is already on the device surface. The MIX data type consists of two binary raster operation (ROP2) values packed into a single ULONG. The lowest-order byte defines the foreground raster operation; the next byte defines the background raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556180">DrvBitBlt</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556220">DrvFillPath</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556316">DrvStrokePath</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568195">LINEATTRS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570618">XFORMOBJ</a>
 

 


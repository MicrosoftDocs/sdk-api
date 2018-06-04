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

# DrvStrokePath function


## -description


The <b>DrvStrokePath</b> function strokes (outlines) a path. 


## -parameters




### -param pso [in, out]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure that identifies the surface on which to draw.


### -param ppo [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a> structure. GDI PATHOBJ_<i>Xxx</i> service routines are provided to enumerate the lines, Bezier curves, and other data that make up the path. This indicates what is to be drawn.


### -param pco [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a> structure. GDI CLIPOBJ_<i>Xxx</i> service routines are provided to enumerate the <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a> as a set of rectangles. Optionally, all the lines in the path may be enumerated preclipped in a CLIPOBJ structure. This means that drivers can have GDI perform all line clipping calculations.


### -param pxo [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570618">XFORMOBJ</a> structure. This is needed only when a geometric wide line is to be drawn. It specifies the transform that maps world coordinates to device coordinates. This is needed because the path is provided in device coordinates but a geometric wide line is actually widened in world coordinates.

The XFORMOBJ structure can be queried to find the transform.


### -param pbo [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a> structure that specifies the brush to be used when drawing the path.


### -param pptlBrushOrg [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that specifies the brush origin used to align the brush pattern on the device.


### -param plineattrs [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568195">LINEATTRS</a> structure. Note that the <b>elStyleState</b> member of this structure must be updated as part of this function if the line is styled. Also note that the <b>ptlLastPel</b> member must be updated if a single pixel width cosmetic line is being drawn.


### -param mix [in]

The mix mode that defines the foreground and background raster operations to use for the brush. For more information about mix mode, see Remarks. 


## -returns



The return value is <b>TRUE</b> if the driver is able to stroke the path. If GDI should instead stroke the path, the return value is <b>FALSE</b>, but no error code is logged. If the driver encounters an error, the return value is DDI_ERROR, and an error code is reported.




## -remarks



If the driver has hooked the function, and if the appropriate GCAPS are set, GDI calls <b>DrvStrokePath</b> when GDI draws a line or curve with any set of attributes.

If a driver supports this entry point, it should also support the drawing of cosmetic wide lines with arbitrary clipping. Using the provided GDI functions, the call can be broken down into a set of single-pixel-width lines with precomputed clipping.

This function is required if any drawing is to be done on a <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device-managed surface</a>.

Drivers for advanced devices can optionally receive this call to draw paths containing Bezier curves and geometric wide lines. GDI will test the GCAPS_BEZIERS and GCAPS_GEOMETRICWIDE flags of the <b>flGraphicsCaps</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552835">DEVINFO</a> structure to decide whether it should call this function. (The four combinations of the bits determine the four levels of functionality for this call.) If the driver gets an advanced call containing Bezier curves or geometric wide lines, it can decide not to handle the call, returning <b>FALSE</b>. This might happen if the path or clipping is too complex for the device to process. If the call does return <b>FALSE</b>, GDI breaks the call down into simpler calls that can be handled more easily.

For device-managed surfaces, the function must minimally support single-pixel-wide solid and styled cosmetic lines using a solid-colored brush.

The mix mode defines how the incoming pattern should be mixed with the data that is already on the device surface. The MIX data type consists of two binary raster operation (ROP2) values packed into a single ULONG. The lowest-order byte defines the foreground raster operation; the next byte defines the background raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552835">DEVINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556220">DrvFillPath</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568195">LINEATTRS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570618">XFORMOBJ</a>
 

 


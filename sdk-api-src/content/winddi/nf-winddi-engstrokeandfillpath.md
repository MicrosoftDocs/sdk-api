---
UID: NF:winddi.EngStrokeAndFillPath
title: EngStrokeAndFillPath function
author: windows-sdk-content
description: The EngStrokeAndFillPath function causes GDI to fill a path and stroke it at the same time.
old-location: display\engstrokeandfillpath.htm
old-project: display
ms.assetid: a58ce829-aa55-46d6-b6d0-205140a9548c
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EngStrokeAndFillPath, EngStrokeAndFillPath function [Display Devices], display.engstrokeandfillpath, gdifncs_aad2693d-6a0e-40ab-ad95-aa38e77c7651.xml, winddi/EngStrokeAndFillPath
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	EngStrokeAndFillPath
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngStrokeAndFillPath function


## -description


The <b>EngStrokeAndFillPath</b> function causes GDI to fill a path and stroke it at the same time.


## -parameters




### -param pso

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure that defines the drawing surface.


### -param ppo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a> structure that defines the path to be filled. The <b>PATHOBJ_</b><i>Xxx</i> service routines are provided to enumerate the lines, Bezier curves, and other data that make up the path.


### -param pco

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a> structure. The <b>CLIPOBJ_</b><i>Xxx</i> service routines are provided to enumerate the <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a> as a set of rectangles.


### -param pxo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff570618">XFORMOBJ</a> structure that is only needed when a geometric wide line is to be drawn and specifies the transform that converts world coordinates to device coordinates. The path is provided in device coordinates but a geometric wide line is actually widened in world coordinates.

The driver can use the <b>XFORMOBJ_</b><i>Xxx</i> service routines to determine the transform.


### -param pboStroke

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a> structure that describes the brush to use when stroking the path.


### -param plineattrs

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568195">LINEATTRS</a> structure.


### -param pboFill

Pointer to a BRUSHOBJ structure that describes the brush to use when filling the path.


### -param pptlBrushOrg

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569166">POINTL</a> structure that defines the brush origin for both brushes.


### -param mixFill [in]

Defines the foreground and background raster operations to use for the fill brush.


### -param flOptions [in]

Specifies which fill mode to use. This parameter can be FP_WINDINGMODE or FP_ALTERNATEMODE; all other bits should be ignored. For more information about these modes, see <a href="https://msdn.microsoft.com/fa1fb4b9-5ed6-44a2-8a9e-0c1c82f5ea39">Path Fill Modes</a>.


## -returns



The return value is <b>TRUE</b> if GDI fills the path. If the driver should fill the path, the return value is <b>FALSE</b>, and an error code is not logged. If GDI encounters an unexpected error, such as not being able to realize the brush, the return value is DDI_ERROR, and an error code is logged.




## -remarks



The mix mode defines how the incoming pattern should be mixed with the data already on the device surface. The MIX data type consists of two ROP2 values packed into a single ULONG. The low-order byte defines the foreground raster operation; the next byte defines the background raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538261">BRUSHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff539417">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556311">DrvStrokeAndFillPath</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568195">LINEATTRS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570618">XFORMOBJ</a>
 

 


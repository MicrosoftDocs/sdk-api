---
UID: NF:winddi.DrvStrokeAndFillPath
title: DrvStrokeAndFillPath function
author: windows-sdk-content
description: The DrvStrokeAndFillPath function strokes (outlines) and fills a path concurrently.
old-location: display\drvstrokeandfillpath.htm
old-project: display
ms.assetid: 92a04fe5-146d-4839-a854-1ac50705b447
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DrvStrokeAndFillPath, DrvStrokeAndFillPath function [Display Devices], ddifncs_ca3b1895-31d0-4c1b-b47c-df61ccef2afa.xml, display.drvstrokeandfillpath, winddi/DrvStrokeAndFillPath
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvStrokeAndFillPath
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvStrokeAndFillPath function


## -description


The <b>DrvStrokeAndFillPath</b> function strokes (outlines) and fills a path concurrently.


## -parameters




### -param pso [in, out]

Pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that describes the surface on which to draw.


### -param ppo [in, out]

Pointer to a <a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a> structure that describes the path to be filled. The PATHOBJ_<i>Xxx</i> service routines are provided to enumerate the lines, Bezier curves, and other data that make up the path.


### -param pco [in]

Pointer to a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure. The CLIPOBJ_<i>Xxx</i> service routines are provided to enumerate the <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a> as a set of rectangles.


### -param pxo [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/a18af8fc-880a-4ac3-905a-1d9384c2b8d7">XFORMOBJ</a> structure that is required when a geometric wide line is drawn. It specifies the transform that takes world coordinates to device coordinates. This is needed because the path is provided in device coordinates but a geometric wide line is actually widened in world coordinates. The XFORMOBJ can be queried to find out what the transform is.


### -param pboStroke [in]

Pointer to a <a href="https://msdn.microsoft.com/81216bee-d13f-4880-a839-337a247a6c82">BRUSHOBJ</a> structure that specifies the brush to use when stroking the path.


### -param plineattrs [in]

Pointer to the <a href="https://msdn.microsoft.com/40fcd6e2-7ed4-433f-ab8b-cc75a305adb9">LINEATTRS</a> structure that describes the attributes of the line to be drawn.


### -param pboFill [in]

Pointer to a BRUSHOBJ structure that specifies the brush to use when filling the path.


### -param pptlBrushOrg [in]

Pointer to a <a href="https://msdn.microsoft.com/68cd23d7-7898-4132-abfe-4dda527889b9">POINTL</a> structure that specifies the brush origin for both brushes.


### -param mixFill [in]

The mix mode that defines the foreground and background raster operations to use for the brush. For more information about mix mode, see Remarks. 


### -param flOptions [in]

Specifies either FP_WINDINGMODE, meaning that a winding mode fill should be performed, or FP_ALTERNATEMODE, meaning that an alternating mode fill should be performed. All other flags should be ignored. For more information about these modes, see <a href="https://msdn.microsoft.com/fa1fb4b9-5ed6-44a2-8a9e-0c1c82f5ea39">Path Fill Modes</a>.


## -returns



The return value is <b>TRUE</b> if the driver is able to fill the path. Otherwise, if GDI should instead fill the path, the return value is <b>FALSE</b>. If an error occurs, the return value is DDI_ERROR, and an error code is logged.




## -remarks



If a wide line is used for stroking, the filled area must be reduced to compensate.

The driver can return <b>FALSE</b> if the path or the clipping is too complex for the device to handle; in that case, GDI converts to a simpler call. For example, if the device driver has set the GCAPS_BEZIERS flag in the <b>flGraphicsCaps</b> member of the <a href="https://msdn.microsoft.com/5ba3e521-2e70-4a5b-979d-30a061275d42">DEVINFO</a> structure and then receives a path with Bezier curves, it can return <b>FALSE</b>; GDI will then convert the Bezier curves to lines and call <b>DrvStrokeAndFillPath</b> again. If the device driver returns <b>FALSE</b> again, GDI will further simplify the call, making calls to <a href="https://msdn.microsoft.com/c931a39d-c0ae-4f40-b70f-f51d5621c228">DrvStrokePath</a> and <a href="https://msdn.microsoft.com/6f499d08-d2a1-46d0-b931-e6c16c4e1d3a">DrvFillPath</a>, or to <a href="https://msdn.microsoft.com/d7b4e25c-b9a1-4200-b449-b7c7ed059db4">DrvBitBlt</a>, depending on the mix and width of the lines making up the path.

The mix mode defines how the incoming pattern should be mixed with the data that is already on the device surface. The MIX data type consists of two binary raster operation (ROP2) values packed into a single ULONG. The lowest-order byte defines the foreground raster operation; the next byte defines the background raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/d7b4e25c-b9a1-4200-b449-b7c7ed059db4">DrvBitBlt</a>



<a href="https://msdn.microsoft.com/6f499d08-d2a1-46d0-b931-e6c16c4e1d3a">DrvFillPath</a>



<a href="https://msdn.microsoft.com/c931a39d-c0ae-4f40-b70f-f51d5621c228">DrvStrokePath</a>



<a href="https://msdn.microsoft.com/40fcd6e2-7ed4-433f-ab8b-cc75a305adb9">LINEATTRS</a>



<a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a>



<a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a>



<a href="https://msdn.microsoft.com/a18af8fc-880a-4ac3-905a-1d9384c2b8d7">XFORMOBJ</a>
 

 


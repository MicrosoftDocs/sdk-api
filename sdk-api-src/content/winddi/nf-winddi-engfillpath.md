---
UID: NF:winddi.EngFillPath
title: EngFillPath function
author: windows-sdk-content
description: The EngFillPath function fills a path.
old-location: display\engfillpath.htm
old-project: display
ms.assetid: 81c4ae89-391c-482b-b5dc-ef34d41607a1
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: EngFillPath, EngFillPath function [Display Devices], display.engfillpath, gdifncs_5128f1e3-265b-4570-8504-1782a07268d5.xml, winddi/EngFillPath
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngFillPath function


## -description


The <b>EngFillPath</b> function fills a path. 


## -parameters




### -param pso

Pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that describes the surface on which to draw.


### -param ppo

Pointer to a <a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a> structure that defines the path to be filled. Use the <b>PATHOBJ_</b><i>Xxx</i> service routines to enumerate the lines, Bezier curves, and other data that make up the path.


### -param pco

Pointer to a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure. Use the <b>CLIPOBJ_</b><i>Xxx</i> service routines to enumerate the <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a> as a set of rectangles.


### -param pbo

Pointer to a <a href="https://msdn.microsoft.com/81216bee-d13f-4880-a839-337a247a6c82">BRUSHOBJ</a> structure that defines the pattern and colors with which to fill.


### -param pptlBrushOrg

Pointer to a <a href="https://msdn.microsoft.com/68cd23d7-7898-4132-abfe-4dda527889b9">POINTL</a> structure defining the brush origin to use to align the brush pattern on the device.


### -param mix [in]

Defines the foreground and background raster operations to use for the brush.


### -param flOptions [in]

Specifies the mode to use when filling the path. This value should be FP_WINDINGMODE or FP_ALTERNATEMODE. All other flags should be ignored. For more information about these modes, see <a href="https://msdn.microsoft.com/fa1fb4b9-5ed6-44a2-8a9e-0c1c82f5ea39">Path Fill Modes</a>.


## -returns



The return value is <b>TRUE</b> if GDI is able to fill the path. Otherwise, it is <b>FALSE</b>, and an error code is not logged. If an error is encountered, the return value is <b>FALSE</b>, and an error code is logged.




## -remarks



Whenever GDI fills a path on a <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device-managed surface</a>, it can call this entry point depending on a comparison of the fill requirements and the following GCAPS bits: GCAPS_BEZIERS, GCAPS_ALTERNATEFILL, and GCAPS_WINDINGFILL.




## -see-also




<a href="https://msdn.microsoft.com/81216bee-d13f-4880-a839-337a247a6c82">BRUSHOBJ</a>



<a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a>



<a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a>
 

 


---
UID: NF:winddi.EngPaint
title: EngPaint function
author: windows-sdk-content
description: The EngPaint function causes GDI to paint a specified region.
old-location: display\engpaint.htm
old-project: display
ms.assetid: 9bfa2e7b-06c7-427a-9283-54b9c6cdac30
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: EngPaint, EngPaint function [Display Devices], display.engpaint, gdifncs_fdbafee3-278d-4d69-bd16-535e92436a1d.xml, winddi/EngPaint
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
 - EngPaint
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngPaint function


## -description


The <b>EngPaint</b> function causes GDI to paint a specified region.


## -parameters




### -param pso

Pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that describes the surface on which to draw.


### -param pco

Pointer to a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure that defines the area to be painted. The <b>CLIPOBJ_</b><i>Xxx</i> service routines are provided to enumerate the <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a> as a set of rectangles.


### -param pbo

Pointer to a <a href="https://msdn.microsoft.com/81216bee-d13f-4880-a839-337a247a6c82">BRUSHOBJ</a> structure that defines the pattern and colors with which to fill.


### -param pptlBrushOrg

Pointer to a <a href="https://msdn.microsoft.com/68cd23d7-7898-4132-abfe-4dda527889b9">POINTL</a> structure that defines the brush origin used to align the brush pattern on the device.


### -param mix [in]

Defines the foreground and background raster operations to use for the brush.


## -returns



The return value is <b>TRUE</b> if the function is successful. Otherwise, it is <b>FALSE</b>, and an error code is logged.




## -remarks



Vector device drivers can implement this function with the help of <a href="https://msdn.microsoft.com/b41f77cb-5dd6-43bd-86dc-0bbcbb3e9f6a">EngCreatePath</a> and <b>PATHOBJ_</b><i>Xxx</i> service routines.

The mix mode defines how the incoming pattern should be mixed with the data already on the device surface. The MIX data type consists of two ROP2 values packed into a single ULONG. The low-order byte defines the foreground raster operation; the next byte defines the background raster operation. For more information about raster operation codes, see the Microsoft Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/81216bee-d13f-4880-a839-337a247a6c82">BRUSHOBJ</a>



<a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/b41f77cb-5dd6-43bd-86dc-0bbcbb3e9f6a">EngCreatePath</a>



<a href="https://msdn.microsoft.com/ceccca92-3312-49b4-b0f6-a3d0cd4bbef5">PATHOBJ</a>



<a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a>
 

 


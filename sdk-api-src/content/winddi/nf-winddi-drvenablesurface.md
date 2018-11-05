---
UID: NF:winddi.DrvEnableSurface
title: DrvEnableSurface function
author: windows-sdk-content
description: The DrvEnableSurface function sets up a surface to be drawn on and associates it with a given physical device.
old-location: display\drvenablesurface.htm
tech.root: display
ms.assetid: a838a44a-243c-4d0d-bda3-eec9a626cb53
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DrvEnableSurface, DrvEnableSurface function [Display Devices], ddifncs_c0044970-ac75-4dae-af55-f6fd87079dbb.xml, display.drvenablesurface, winddi/DrvEnableSurface
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
 - DrvEnableSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvEnableSurface function


## -description


The <b>DrvEnableSurface</b> function sets up a surface to be drawn on and associates it with a given physical device.


## -parameters




### -param dhpdev

Handle to the physical device's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>. This is the return value of <a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>. The PDEV describes the physical device for which a surface is to be created.


## -returns



The return value is a handle that identifies the newly created surface. Otherwise, it is zero, and an error code is logged.




## -remarks



There are two methods for preparing a surface for use. 

<ol>
<li>
In this method, which is recommended, the driver creates the surface by a call to <a href="https://msdn.microsoft.com/9c3ca4c4-7614-4739-8333-202c6ec2eab8">EngCreateDeviceSurface</a>. After GDI creates the surface and returns a handle to the driver, the driver calls <a href="https://msdn.microsoft.com/176f51c0-0075-4afb-8b5c-5d0b6b64a3ad">EngModifySurface</a>, which sets the appropriate hook flags, and optionally, informs GDI of the surface's location.

</li>
<li>
The second method is the one used by Windows NT 4.0 drivers. In this method, the driver calls <a href="https://msdn.microsoft.com/51da3fbc-bf6e-47a9-8ee8-ebf34c23b66c">EngCreateBitmap</a>. After this call, the driver calls <a href="https://msdn.microsoft.com/8cb6d4bf-67bd-4bfb-9605-eeb954fc590c">EngAssociateSurface</a> to associate the surface with the physical display device. This GDI function allows the driver to specify which graphics output routines are supported for standard-format bitmaps. A call to this function can be made only when no surface exists for the given physical device. If a Windows 2000 or later driver is back-ported to run on Windows NT 4.0, this method must be used. If such a driver will also run on Windows 2000 or later, a separate code path in the driver should use the first method. 

For printer devices, the usual situation is for GDI to collect the graphics directly onto a GDI bitmap. The driver should call <a href="https://msdn.microsoft.com/51da3fbc-bf6e-47a9-8ee8-ebf34c23b66c">EngCreateBitmap</a>, which allows GDI to allocate memory for the bitmap.

</li>
</ol>
Any existing GDI bitmap handle is a valid surface handle.

For <a href="https://msdn.microsoft.com/58e181ff-c792-41a5-967d-a69a8ff5a041">printer graphics DLLs</a> that use GDI-managed surfaces, the <b>DrvEnableSurface</b> function should call <a href="https://msdn.microsoft.com/51da3fbc-bf6e-47a9-8ee8-ebf34c23b66c">EngCreateBitmap</a>, specifying a surface size large enough to contain an entire physical page. If that fails, repeated calls to <b>EngCreateBitmap</b> should be attempted, with decreasing surface sizes, until a call succeeds. The valid size should be specified as input to <a href="https://msdn.microsoft.com/0ee3d697-42aa-4117-9d85-63472e4a042f">EngMarkBandingSurface</a>, which informs GDI that surface banding will be necessary.

After <b>DrvEnableSurface</b> returns a handle to a primary surface, do not call <a href="https://msdn.microsoft.com/176f51c0-0075-4afb-8b5c-5d0b6b64a3ad">EngModifySurface</a> or <a href="https://msdn.microsoft.com/8cb6d4bf-67bd-4bfb-9605-eeb954fc590c">EngAssociateSurface</a> on that handle. Doing so can cause a bug check in certain circumstances. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=3100&amp;ID=330248">Microsoft Knowledge Base article 330248</a>.

<b>DrvEnableSurface</b> is required for graphics drivers.




## -see-also




<a href="https://msdn.microsoft.com/18714107-7287-4d50-a2f9-b5d72f111f8b">DrvDisableSurface</a>



<a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/51da3fbc-bf6e-47a9-8ee8-ebf34c23b66c">EngCreateBitmap</a>



<a href="https://msdn.microsoft.com/9c3ca4c4-7614-4739-8333-202c6ec2eab8">EngCreateDeviceSurface</a>
 

 


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

# EngMarkBandingSurface function


## -description


The <b>EngMarkBandingSurface </b>function marks the specified surface as a banding surface.


## -parameters




### -param hsurf [in]

Caller-supplied handle to the surface to mark as a banding surface.


## -returns



<b>EngMarkBandingSurface</b> returns <b>TRUE</b> upon success; otherwise it returns <b>FALSE</b>.




## -remarks



If a <a href="https://msdn.microsoft.com/58e181ff-c792-41a5-967d-a69a8ff5a041">printer graphics DLL</a> uses GDI-managed surfaces, it must call <b>EngMarkBandingSurface</b> if it cannot create a surface (by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff564199">EngCreateBitmap</a>) that is large enough to hold an entire physical page's bitmap. Both <b>EngCreateBitmap</b> and <b>EngMarkBandingSurface</b> should be called from within the printer graphics DLL's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556214">DrvEnableSurface</a> function.

The handle supplied for <i>hsurf</i> must be a bitmap handle returned by <b>EngCreateBitmap</b>.

If a printer graphics DLL calls <b>EngMarkBandingSurface</b>, it must define <a href="https://msdn.microsoft.com/library/windows/hardware/ff556292">DrvStartBanding</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff556250">DrvNextBand</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556214">DrvEnableSurface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556250">DrvNextBand</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556292">DrvStartBanding</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564199">EngCreateBitmap</a>
 

 


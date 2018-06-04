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

# VMRRenderPrefs enumeration


## -description



The <b>VMRRenderPrefs</b> enumeration type is used with the <a href="https://msdn.microsoft.com/aabf3628-3179-430c-a74b-0cb4e552cbe2">IVMRFilterConfig::GetRenderingPrefs</a> and <a href="https://msdn.microsoft.com/1374d071-f396-4fcb-8ca2-ac3986960207">IVMRFilterConfig::SetRenderingPrefs</a> methods to get and set basic rendering preferences.




## -enum-fields




### -field RenderPrefs_RestrictToInitialMonitor


            Not implemented; do not use.
          


### -field RenderPrefs_ForceOffscreen


            Indicates that the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7) should use only offscreen surfaces for rendering.
          


### -field RenderPrefs_ForceOverlays


            Indicates that the VMR-7 should fail if no overlay surfaces are available.
          


### -field RenderPrefs_AllowOverlays


            Indicates that the VMR-7 should use overlays if they are available. Should not be used by new applications.
          


### -field RenderPrefs_AllowOffscreen

Indicates that the VMR-7 should use offscreen surfaces if no overlays are available. Should not be used by new applications.


### -field RenderPrefs_DoNotRenderColorKeyAndBorder


            Indicates that the application is responsible for painting the color keys.
          


### -field RenderPrefs_Reserved


            Reserved; do not use.
          


### -field RenderPrefs_PreferAGPMemWhenMixing

Indicates that the VMR-7 should attempt to use AGP memory when allocating texture surfaces.


### -field RenderPrefs_Mask


            Bitwise <b>OR</b> of all of the above flags.
          


## -remarks



By default the VMR-7 tries to allocate DirectDraw texture surfaces from Video Memory and falls back to AGP memory if there is no Video Memory remaining to fulfill the allocation. In order for the VMR-7 to use AGP memory, the graphics card must have some basic support for blitting from AGP memory to Video Memory.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 


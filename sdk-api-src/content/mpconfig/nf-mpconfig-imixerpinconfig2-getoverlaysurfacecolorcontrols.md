---
UID: NF:mpconfig.IMixerPinConfig2.GetOverlaySurfaceColorControls
title: IMixerPinConfig2::GetOverlaySurfaceColorControls
author: windows-sdk-content
description: The GetOverlaySurfaceColorControls method retrieves the color control settings associated with the specified overlay surface.
old-location: dshow\imixerpinconfig2_getoverlaysurfacecolorcontrols.htm
old-project: DirectShow
ms.assetid: c6b47e4d-5bf2-4d76-a1e2-88a3342d75a6
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetOverlaySurfaceColorControls, GetOverlaySurfaceColorControls method [DirectShow], GetOverlaySurfaceColorControls method [DirectShow],IMixerPinConfig2 interface, IMixerPinConfig2 interface [DirectShow],GetOverlaySurfaceColorControls method, IMixerPinConfig2.GetOverlaySurfaceColorControls, IMixerPinConfig2::GetOverlaySurfaceColorControls, IMixerPinConfig2GetOverlaySurfaceColorControls, dshow.imixerpinconfig2_getoverlaysurfacecolorcontrols, mpconfig/IMixerPinConfig2::GetOverlaySurfaceColorControls
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mpconfig.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: AM_ASPECT_RATIO_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMixerPinConfig2.GetOverlaySurfaceColorControls
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMixerPinConfig2::GetOverlaySurfaceColorControls


## -description



The <code>GetOverlaySurfaceColorControls</code> method retrieves the color control settings associated with the specified overlay surface.




## -parameters




### -param pColorControl [out]

Address of a pointer to the <b>DDCOLORCONTROL</b> structure containing the color values currently applied to the specified surface.


## -returns



Returns an <b>HRESULT</b> value. If the allocator on the pin is not using an overlay surface, the method returns E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d166b139-3ef7-4f47-817a-8f5b644a3776">IMixerPinConfig2 Interface</a>
 

 


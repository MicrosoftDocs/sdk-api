---
UID: NF:mpconfig.IMixerPinConfig2.SetOverlaySurfaceColorControls
title: IMixerPinConfig2::SetOverlaySurfaceColorControls
author: windows-sdk-content
description: Sets the color control settings associated with the specified overlay surface.
old-location: dshow\imixerpinconfig2_setoverlaysurfacecolorcontrols.htm
old-project: DirectShow
ms.assetid: c23c12c9-5621-4b1e-997a-51303f239175
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IMixerPinConfig2 interface [DirectShow],SetOverlaySurfaceColorControls method, IMixerPinConfig2.SetOverlaySurfaceColorControls, IMixerPinConfig2::SetOverlaySurfaceColorControls, IMixerPinConfig2SetOverlaySurfaceColorControls, SetOverlaySurfaceColorControls, SetOverlaySurfaceColorControls method [DirectShow], SetOverlaySurfaceColorControls method [DirectShow],IMixerPinConfig2 interface, dshow.imixerpinconfig2_setoverlaysurfacecolorcontrols, mpconfig/IMixerPinConfig2::SetOverlaySurfaceColorControls
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
 - IMixerPinConfig2.SetOverlaySurfaceColorControls
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMixerPinConfig2::SetOverlaySurfaceColorControls


## -description



Sets the color control settings associated with the specified overlay surface.




## -parameters




### -param pColorControl [in]

Address of a pointer to the <b>DDCOLORCONTROL</b> structure containing the new values to be applied to the specified surface.


## -returns



Returns an <b>HRESULT</b> value. If the allocator on the pin is not using an overlay surface, the method returns E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d166b139-3ef7-4f47-817a-8f5b644a3776">IMixerPinConfig2 Interface</a>
 

 


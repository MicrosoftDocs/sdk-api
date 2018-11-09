---
UID: NF:vpconfig.IVPBaseConfig.SetSurfaceParameters
title: IVPBaseConfig::SetSurfaceParameters
author: windows-sdk-content
description: The SetSurfaceParameters method informs the device of the layout of the overlay surface. The downstream filter (the Overlay Mixer, VBI Surface Allocator, or Video Port Manager) calls this method after it creates the overlay surface.
old-location: dshow\ivpbaseconfig_setsurfaceparameters.htm
tech.root: DirectShow
ms.assetid: 4af0092e-5866-45ca-b0be-e97d9dd51b0f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IVPBaseConfig interface [DirectShow],SetSurfaceParameters method, IVPBaseConfig.SetSurfaceParameters, IVPBaseConfig::SetSurfaceParameters, IVPBaseConfigSetSurfaceParameters, SetSurfaceParameters, SetSurfaceParameters method [DirectShow], SetSurfaceParameters method [DirectShow],IVPBaseConfig interface, dshow.ivpbaseconfig_setsurfaceparameters, vpconfig/IVPBaseConfig::SetSurfaceParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vpconfig.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vpconfig.h
api_name:
 - IVPBaseConfig.SetSurfaceParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVPBaseConfig::SetSurfaceParameters


## -description



The <code>SetSurfaceParameters</code> method informs the device of the layout of the overlay surface. The downstream filter (the Overlay Mixer, VBI Surface Allocator, or Video Port Manager) calls this method after it creates the overlay surface.




## -parameters




### -param dwPitch [in]

Specifies the stride of the surface (also called the <i>pitch</i>), in pixels.


### -param dwXOrigin [in]

Specifies the X-coordinate of the pixel at which valid data starts.


### -param dwYOrigin [in]

Specifies the Y-coordinate of the pixel at which valid data starts.


## -returns



Returns S_OK if successful, or E_NOTIMPL.




## -remarks



Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d9a4f395-3d2f-429a-884d-90131927a929">IVPBaseConfig Interface</a>
 

 


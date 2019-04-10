---
UID: NF:vpconfig.IVPBaseConfig.SetDDSurfaceKernelHandles
title: IVPBaseConfig::SetDDSurfaceKernelHandles (vpconfig.h)
author: windows-sdk-content
description: The SetDDSurfaceKernelHandles method specifies the kernel-mode handles of the DirectDraw surfaces to be used for the overlay suface.
old-location: dshow\ivpbaseconfig_setddsurfacekernelhandles.htm
tech.root: DirectShow
ms.assetid: e180f731-a540-4754-93ff-232ad4502c6f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVPBaseConfig interface [DirectShow],SetDDSurfaceKernelHandles method, IVPBaseConfig.SetDDSurfaceKernelHandles, IVPBaseConfig::SetDDSurfaceKernelHandles, IVPBaseConfigSetDDSurfaceKernelHandle, SetDDSurfaceKernelHandles, SetDDSurfaceKernelHandles method [DirectShow], SetDDSurfaceKernelHandles method [DirectShow],IVPBaseConfig interface, dshow.ivpbaseconfig_setddsurfacekernelhandles, vpconfig/IVPBaseConfig::SetDDSurfaceKernelHandles
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
 - IVPBaseConfig.SetDDSurfaceKernelHandles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVPBaseConfig::SetDDSurfaceKernelHandles


## -description



The <code>SetDDSurfaceKernelHandles</code> method specifies the kernel-mode handles of the DirectDraw surfaces to be used for the overlay suface.




## -parameters




### -param cHandles [in]

Specifies the number of handles in the <i>rgDDKernelHandles</i> array.


### -param rgDDKernelHandles [in]

Address of an array of kernel-mode handles.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method sets the DirectDraw handles for the overlay surface. There may be more than one attached surface, so the array may contain more than one surface handle.

Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd390567(v=VS.85).aspx">IVPBaseConfig Interface</a>
 

 


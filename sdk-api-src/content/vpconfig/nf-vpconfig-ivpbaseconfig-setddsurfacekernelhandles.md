---
UID: NF:vpconfig.IVPBaseConfig.SetDDSurfaceKernelHandles
title: IVPBaseConfig::SetDDSurfaceKernelHandles
author: windows-driver-content
description: The SetDDSurfaceKernelHandles method specifies the kernel-mode handles of the DirectDraw surfaces to be used for the overlay suface.
old-location: dshow\ivpbaseconfig_setddsurfacekernelhandles.htm
old-project: DirectShow
ms.assetid: e180f731-a540-4754-93ff-232ad4502c6f
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IVPBaseConfig interface [DirectShow],SetDDSurfaceKernelHandles method, IVPBaseConfig.SetDDSurfaceKernelHandles, IVPBaseConfig::SetDDSurfaceKernelHandles, IVPBaseConfigSetDDSurfaceKernelHandle, SetDDSurfaceKernelHandles, SetDDSurfaceKernelHandles method [DirectShow], SetDDSurfaceKernelHandles method [DirectShow],IVPBaseConfig interface, dshow.ivpbaseconfig_setddsurfacekernelhandles, vpconfig/IVPBaseConfig::SetDDSurfaceKernelHandles
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
req.typenames: VMR9VideoStreamInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Vpconfig.h
api_name:
-	IVPBaseConfig.SetDDSurfaceKernelHandles
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
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



<a href="https://msdn.microsoft.com/d9a4f395-3d2f-429a-884d-90131927a929">IVPBaseConfig Interface</a>
 

 


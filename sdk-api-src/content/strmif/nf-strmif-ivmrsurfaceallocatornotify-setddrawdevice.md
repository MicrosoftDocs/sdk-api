---
UID: NF:strmif.IVMRSurfaceAllocatorNotify.SetDDrawDevice
title: IVMRSurfaceAllocatorNotify::SetDDrawDevice
author: windows-sdk-content
description: The SetDDrawDevice method sets the initial DirectDraw device and monitor to be used for video playback.
old-location: dshow\ivmrsurfaceallocatornotify_setddrawdevice.htm
old-project: DirectShow
ms.assetid: 3e6bd77e-8b2d-4cd8-9bd3-40a3fe9373f3
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IVMRSurfaceAllocatorNotify interface [DirectShow],SetDDrawDevice method, IVMRSurfaceAllocatorNotify.SetDDrawDevice, IVMRSurfaceAllocatorNotify::SetDDrawDevice, IVMRSurfaceAllocatorNotifySetDDrawDevice, SetDDrawDevice, SetDDrawDevice method [DirectShow], SetDDrawDevice method [DirectShow],IVMRSurfaceAllocatorNotify interface, dshow.ivmrsurfaceallocatornotify_setddrawdevice, strmif/IVMRSurfaceAllocatorNotify::SetDDrawDevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRSurfaceAllocatorNotify.SetDDrawDevice
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRSurfaceAllocatorNotify::SetDDrawDevice


## -description



The <code>SetDDrawDevice</code> method sets the initial DirectDraw device and monitor to be used for video playback.




## -parameters




### -param lpDDrawDevice




### -param hMonitor [in]

Handle to the monitor associated with the DirectDraw device.


#### - lpDirectDrawDevice [in]

Specifies the DirectDraw device.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The VMR needs to know which DirectDraw device is being used at any given time in order to associate the Direct3D surfaces being created in the mixer component with that device.




## -see-also




<a href="https://msdn.microsoft.com/c590c4cb-43ba-41c2-ab1f-28f7aeee0c87">IVMRSurfaceAllocatorNotify Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 


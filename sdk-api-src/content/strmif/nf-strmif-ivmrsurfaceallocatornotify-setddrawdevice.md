---
UID: NF:strmif.IVMRSurfaceAllocatorNotify.SetDDrawDevice
title: IVMRSurfaceAllocatorNotify::SetDDrawDevice (strmif.h)
description: The SetDDrawDevice method sets the initial DirectDraw device and monitor to be used for video playback.
helpviewer_keywords: ["IVMRSurfaceAllocatorNotify interface [DirectShow]","SetDDrawDevice method","IVMRSurfaceAllocatorNotify.SetDDrawDevice","IVMRSurfaceAllocatorNotify::SetDDrawDevice","IVMRSurfaceAllocatorNotifySetDDrawDevice","SetDDrawDevice","SetDDrawDevice method [DirectShow]","SetDDrawDevice method [DirectShow]","IVMRSurfaceAllocatorNotify interface","dshow.ivmrsurfaceallocatornotify_setddrawdevice","strmif/IVMRSurfaceAllocatorNotify::SetDDrawDevice"]
old-location: dshow\ivmrsurfaceallocatornotify_setddrawdevice.htm
tech.root: dshow
ms.assetid: 3e6bd77e-8b2d-4cd8-9bd3-40a3fe9373f3
ms.date: 12/05/2018
ms.keywords: IVMRSurfaceAllocatorNotify interface [DirectShow],SetDDrawDevice method, IVMRSurfaceAllocatorNotify.SetDDrawDevice, IVMRSurfaceAllocatorNotify::SetDDrawDevice, IVMRSurfaceAllocatorNotifySetDDrawDevice, SetDDrawDevice, SetDDrawDevice method [DirectShow], SetDDrawDevice method [DirectShow],IVMRSurfaceAllocatorNotify interface, dshow.ivmrsurfaceallocatornotify_setddrawdevice, strmif/IVMRSurfaceAllocatorNotify::SetDDrawDevice
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVMRSurfaceAllocatorNotify::SetDDrawDevice
 - strmif/IVMRSurfaceAllocatorNotify::SetDDrawDevice
dev_langs:
 - c++
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
---

# IVMRSurfaceAllocatorNotify::SetDDrawDevice


## -description

The <code>SetDDrawDevice</code> method sets the initial DirectDraw device and monitor to be used for video playback.

## -parameters

### -param lpDDrawDevice [in]

Specifies the DirectDraw device.

### -param hMonitor [in]

Handle to the monitor associated with the DirectDraw device.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The VMR needs to know which DirectDraw device is being used at any given time in order to associate the Direct3D surfaces being created in the mixer component with that device.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ivmrsurfaceallocatornotify">IVMRSurfaceAllocatorNotify Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
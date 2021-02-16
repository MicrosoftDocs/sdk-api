---
UID: NF:strmif.IVMRSurfaceAllocatorNotify.ChangeDDrawDevice
title: IVMRSurfaceAllocatorNotify::ChangeDDrawDevice (strmif.h)
description: The ChangeDDrawDevice method notifies the VMR that the DirectDraw playback device has changed. For example, on a multi-monitor system, the user has moved the video rectangle from one monitor to another.
helpviewer_keywords: ["ChangeDDrawDevice","ChangeDDrawDevice method [DirectShow]","ChangeDDrawDevice method [DirectShow]","IVMRSurfaceAllocatorNotify interface","IVMRSurfaceAllocatorNotify interface [DirectShow]","ChangeDDrawDevice method","IVMRSurfaceAllocatorNotify.ChangeDDrawDevice","IVMRSurfaceAllocatorNotify::ChangeDDrawDevice","IVMRSurfaceAllocatorNotifyChangeDDrawDevice","dshow.ivmrsurfaceallocatornotify_changeddrawdevice","strmif/IVMRSurfaceAllocatorNotify::ChangeDDrawDevice"]
old-location: dshow\ivmrsurfaceallocatornotify_changeddrawdevice.htm
tech.root: dshow
ms.assetid: 4fc4a001-7522-45b0-9b55-510f3ee3eb6d
ms.date: 12/05/2018
ms.keywords: ChangeDDrawDevice, ChangeDDrawDevice method [DirectShow], ChangeDDrawDevice method [DirectShow],IVMRSurfaceAllocatorNotify interface, IVMRSurfaceAllocatorNotify interface [DirectShow],ChangeDDrawDevice method, IVMRSurfaceAllocatorNotify.ChangeDDrawDevice, IVMRSurfaceAllocatorNotify::ChangeDDrawDevice, IVMRSurfaceAllocatorNotifyChangeDDrawDevice, dshow.ivmrsurfaceallocatornotify_changeddrawdevice, strmif/IVMRSurfaceAllocatorNotify::ChangeDDrawDevice
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
 - IVMRSurfaceAllocatorNotify::ChangeDDrawDevice
 - strmif/IVMRSurfaceAllocatorNotify::ChangeDDrawDevice
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
 - IVMRSurfaceAllocatorNotify.ChangeDDrawDevice
---

# IVMRSurfaceAllocatorNotify::ChangeDDrawDevice


## -description

The <code>ChangeDDrawDevice</code> method notifies the VMR that the DirectDraw playback device has changed. For example, on a multi-monitor system, the user has moved the video rectangle from one monitor to another.

## -parameters

### -param lpDDrawDevice [in]

Specifies the DirectDraw device.

### -param hMonitor [in]

Specifies the handle to the monitor associated with the DirectDraw device.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The VMR needs to know which DirectDraw device is being used at any given time in order to associate the Direct3D surfaces being created in the mixer component with that device.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ivmrsurfaceallocatornotify">IVMRSurfaceAllocatorNotify Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
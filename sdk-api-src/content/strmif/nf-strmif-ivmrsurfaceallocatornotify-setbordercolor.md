---
UID: NF:strmif.IVMRSurfaceAllocatorNotify.SetBorderColor
title: IVMRSurfaceAllocatorNotify::SetBorderColor (strmif.h)
description: The SetBorderColor method specifies to the VMR which color to use in areas of the display rectangle which are not being used for video, for example when the video is letterboxed.
helpviewer_keywords: ["IVMRSurfaceAllocatorNotify interface [DirectShow]","SetBorderColor method","IVMRSurfaceAllocatorNotify.SetBorderColor","IVMRSurfaceAllocatorNotify::SetBorderColor","IVMRSurfaceAllocatorNotifySetBorderColor","SetBorderColor","SetBorderColor method [DirectShow]","SetBorderColor method [DirectShow]","IVMRSurfaceAllocatorNotify interface","dshow.ivmrsurfaceallocatornotify_setbordercolor","strmif/IVMRSurfaceAllocatorNotify::SetBorderColor"]
old-location: dshow\ivmrsurfaceallocatornotify_setbordercolor.htm
tech.root: dshow
ms.assetid: 29d4b9df-a498-4aff-8e85-51ede64d69dc
ms.date: 12/05/2018
ms.keywords: IVMRSurfaceAllocatorNotify interface [DirectShow],SetBorderColor method, IVMRSurfaceAllocatorNotify.SetBorderColor, IVMRSurfaceAllocatorNotify::SetBorderColor, IVMRSurfaceAllocatorNotifySetBorderColor, SetBorderColor, SetBorderColor method [DirectShow], SetBorderColor method [DirectShow],IVMRSurfaceAllocatorNotify interface, dshow.ivmrsurfaceallocatornotify_setbordercolor, strmif/IVMRSurfaceAllocatorNotify::SetBorderColor
f1_keywords:
- strmif/IVMRSurfaceAllocatorNotify.SetBorderColor
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IVMRSurfaceAllocatorNotify.SetBorderColor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRSurfaceAllocatorNotify::SetBorderColor


## -description



The <code>SetBorderColor</code> method specifies to the VMR which color to use in areas of the display rectangle which are not being used for video, for example when the video is letterboxed.




## -parameters




### -param clrBorder [in]

Specifies the border color.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrsurfaceallocatornotify">IVMRSurfaceAllocatorNotify Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 


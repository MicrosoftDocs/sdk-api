---
UID: NF:strmif.IVMRSurfaceAllocatorNotify.AdviseSurfaceAllocator
title: IVMRSurfaceAllocatorNotify::AdviseSurfaceAllocator
author: windows-sdk-content
description: The AdviseSurfaceAllocator method is called by an application to instruct the VMR to use a custom allocator-presenter.
old-location: dshow\ivmrsurfaceallocatornotify_advisesurfaceallocator.htm
old-project: DirectShow
ms.assetid: fdb0837c-1ee3-4dc9-b797-3d726c8ba3dc
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: AdviseSurfaceAllocator, AdviseSurfaceAllocator method [DirectShow], AdviseSurfaceAllocator method [DirectShow],IVMRSurfaceAllocatorNotify interface, IVMRSurfaceAllocatorNotify interface [DirectShow],AdviseSurfaceAllocator method, IVMRSurfaceAllocatorNotify.AdviseSurfaceAllocator, IVMRSurfaceAllocatorNotify::AdviseSurfaceAllocator, IVMRSurfaceAllocatorNotifyAdviseSurfaceAllocator, dshow.ivmrsurfaceallocatornotify_advisesurfaceallocator, strmif/IVMRSurfaceAllocatorNotify::AdviseSurfaceAllocator
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
 - IVMRSurfaceAllocatorNotify.AdviseSurfaceAllocator
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRSurfaceAllocatorNotify::AdviseSurfaceAllocator


## -description



The <code>AdviseSurfaceAllocator</code> method is called by an application to instruct the VMR to use a custom allocator-presenter.




## -parameters




### -param dwUserID [in]

An application-defined DWORD_PTR that uniquely identifies this instance of the VMR in scenarios when multiple instances of the VMR are being used with a single instance of an allocator-presenter.


### -param lpIVRMSurfaceAllocator






#### - lpIVMRSurfaceAllocator [in]

Specifies the <a href="https://msdn.microsoft.com/bbcbe152-80fd-469b-a79b-c8db6f97da22">IVMRSurfaceAllocator</a> interface on the new allocator-presenter. If this value is <b>NULL</b>, then the VMR will release the client allocator-presenter and restore its default allocator-presenter.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The method will cause the default allocator-presenter to be uninstalled and destroyed, and replaced with the specified new component. The new component must also support the <a href="https://msdn.microsoft.com/cb9b1e29-45c3-4208-8343-c2924505a9f3">IVMRImagePresenter</a> interface.

This method can be called only once in the lifetime of the VMR. The VMR continues to use the allocator-presenter until the VMR is itself deleted. When the VMR is finally released, it releases its reference count on the custom allocator-presenter object, which allows that object to be freed.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/c590c4cb-43ba-41c2-ab1f-28f7aeee0c87">IVMRSurfaceAllocatorNotify Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 


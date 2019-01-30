---
UID: NF:strmif.IVMRSurfaceAllocator.AdviseNotify
title: IVMRSurfaceAllocator::AdviseNotify
author: windows-sdk-content
description: The AdviseNotify method provides the allocator-presenter with the VMR-7 filter's interface for notification callbacks.
old-location: dshow\ivmrsurfaceallocator_advisenotify.htm
tech.root: DirectShow
ms.assetid: d4d9998f-e7d6-4c06-8a37-2e9c8e29106b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AdviseNotify, AdviseNotify method [DirectShow], AdviseNotify method [DirectShow],IVMRSurfaceAllocator interface, IVMRSurfaceAllocator interface [DirectShow],AdviseNotify method, IVMRSurfaceAllocator.AdviseNotify, IVMRSurfaceAllocator::AdviseNotify, IVMRSurfaceAllocatorAdviseNotify, dshow.ivmrsurfaceallocator_advisenotify, strmif/IVMRSurfaceAllocator::AdviseNotify
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
 - IVMRSurfaceAllocator.AdviseNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRSurfaceAllocator::AdviseNotify


## -description



The <code>AdviseNotify</code> method provides the allocator-presenter with the VMR-7 filter's interface for notification callbacks. If you are using a custom allocator-presenter, the application must call this method on the allocator-presenter, with a pointer to the VMR's <b>IVMRSurfaceAllocatorNotify</b> interface. The allocator-presenter uses this interface to communicate with the VMR.



If you are not using a custom allocator-presenter, the application does not have to call this method.


## -parameters




### -param lpIVMRSurfAllocNotify [in]

Specifies the <a href="https://msdn.microsoft.com/c590c4cb-43ba-41c2-ab1f-28f7aeee0c87">IVMRSurfaceAllocatorNotify</a> interface pointer that the allocator-presenter will use to pass notifications back to the VMR.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bbcbe152-80fd-469b-a79b-c8db6f97da22">IVMRSurfaceAllocator Interface</a>



<a href="https://msdn.microsoft.com/19b43c9b-2578-418f-b03b-af7c7a3a46e4">Supplying a Custom Allocator-Presenter for VMR-7</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>



<a href="https://msdn.microsoft.com/0381f862-2f16-4b4d-be48-40f7fe151585">VMR Renderless Playback Mode (Custom Allocator-Presenters)</a>
 

 


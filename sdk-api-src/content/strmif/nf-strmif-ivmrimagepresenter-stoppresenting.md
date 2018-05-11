---
UID: NF:strmif.IVMRImagePresenter.StopPresenting
title: IVMRImagePresenter::StopPresenting
author: windows-driver-content
description: The StopPresenting method is called just after the video stops playing. The allocator-presenter should perform any necessary cleanup in this method.
old-location: dshow\ivmrimagepresenter_stoppresenting.htm
old-project: DirectShow
ms.assetid: b6887c66-56ba-4ee6-a740-73213ac088d5
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IVMRImagePresenter interface [DirectShow],StopPresenting method, IVMRImagePresenter.StopPresenting, IVMRImagePresenter::StopPresenting, IVMRImagePresenterStopPresenting, StopPresenting, StopPresenting method [DirectShow], StopPresenting method [DirectShow],IVMRImagePresenter interface, dshow.ivmrimagepresenter_stoppresenting, strmif/IVMRImagePresenter::StopPresenting
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRImagePresenter.StopPresenting
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRImagePresenter::StopPresenting


## -description



The <code>StopPresenting</code> method is called just after the video stops playing. The allocator-presenter should perform any necessary cleanup in this method.




## -parameters




### -param dwUserID [in]

An application-defined <b>DWORD_PTR</b> cookie that uniquely identifies this instance of the VMR for use in scenarios when one instance of the allocator-presenter is used with multiple VMR instances.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



<code>StopPresenting</code> can be called only when the VMR is in a running state.




## -see-also




<a href="https://msdn.microsoft.com/cb9b1e29-45c3-4208-8343-c2924505a9f3">IVMRImagePresenter Interface</a>



<a href="https://msdn.microsoft.com/b97debae-d792-4c9b-a171-11ef2a73e987">IVMRImagePresenter::StartPresenting</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 


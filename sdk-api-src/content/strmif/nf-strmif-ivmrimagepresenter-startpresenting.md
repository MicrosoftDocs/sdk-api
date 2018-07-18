---
UID: NF:strmif.IVMRImagePresenter.StartPresenting
title: IVMRImagePresenter::StartPresenting
author: windows-sdk-content
description: The StartPresenting method is called just before the video starts playing. The allocator-presenter should perform any necessary configuration in this method.
old-location: dshow\ivmrimagepresenter_startpresenting.htm
old-project: DirectShow
ms.assetid: b97debae-d792-4c9b-a171-11ef2a73e987
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IVMRImagePresenter interface [DirectShow],StartPresenting method, IVMRImagePresenter.StartPresenting, IVMRImagePresenter::StartPresenting, IVMRImagePresenterStartPresenting, StartPresenting, StartPresenting method [DirectShow], StartPresenting method [DirectShow],IVMRImagePresenter interface, dshow.ivmrimagepresenter_startpresenting, strmif/IVMRImagePresenter::StartPresenting
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
 - IVMRImagePresenter.StartPresenting
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRImagePresenter::StartPresenting


## -description



The <code>StartPresenting</code> method is called just before the video starts playing. The allocator-presenter should perform any necessary configuration in this method.




## -parameters




### -param dwUserID [in]

An application-defined <b>DWORD_PTR</b> cookie that uniquely identifies this instance of the VMR for use in scenarios when one instance of the allocator-presenter is used with multiple VMR instances.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



<b>PresentImage</b> can be called when the filter is in either a running or a paused state. <code>StartPresenting</code> and <b>StopPresenting</b> can be called only in a running state. Therefore, if the graph is paused before it is run, <b>PresentImage</b> will be called before <code>StartPresenting</code>.




## -see-also




<a href="https://msdn.microsoft.com/cb9b1e29-45c3-4208-8343-c2924505a9f3">IVMRImagePresenter Interface</a>



<a href="https://msdn.microsoft.com/b6887c66-56ba-4ee6-a740-73213ac088d5">IVMRImagePresenter::StopPresenting</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 


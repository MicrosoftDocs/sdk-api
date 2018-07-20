---
UID: NF:inkpresenterdesktop.IInkDesktopHost.CreateInkPresenter
title: IInkDesktopHost::CreateInkPresenter
author: windows-sdk-content
description: Creates an IInkPresenterDesktop object on an application thread.
old-location: input_ink\iinkdesktophost_createinkpresenter.htm
old-project: input_ink
ms.assetid: 17480bbd-7d4f-4ba9-9d54-80f440104055
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CreateInkPresenter, CreateInkPresenter method, CreateInkPresenter method,IInkDesktopHost interface, IInkDesktopHost interface,CreateInkPresenter method, IInkDesktopHost.CreateInkPresenter, IInkDesktopHost::CreateInkPresenter, InkPresenterDesktop.iinkdesktophost_createinkpresenter, inkpresenterdesktop/IInkDesktopHost::CreateInkPresenter, input_ink.iinkdesktophost_createinkpresenter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: inkpresenterdesktop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: InkPresenterDesktop.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkPresenterDesktop.h
api_name:
 - IInkDesktopHost.CreateInkPresenter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInkDesktopHost::CreateInkPresenter


## -description


Creates an <a href="https://msdn.microsoft.com/6d175981-6379-4a61-84b0-8b08274bc3a3">IInkPresenterDesktop</a> object on an application thread.

The <a href="https://msdn.microsoft.com/6d175981-6379-4a61-84b0-8b08274bc3a3">IInkPresenterDesktop</a> object can then be configured and connected to the app's  <a href="https://msdn.microsoft.com/40e2d02b-77e8-425f-ac5e-3dcddef08173">DirectComposition</a> visual tree. 
<div class="alert"><b>Note</b>  <p class="note">Use <a href="https://msdn.microsoft.com/596e1180-04ca-474b-b519-f9ebe468fb6a">CreateAndInitializeInkPresenter</a> to do this in a single call.

</div><div> </div>

## -parameters




### -param riid [in]

A reference to the interface identifier of an <a href="https://msdn.microsoft.com/6d175981-6379-4a61-84b0-8b08274bc3a3">IInkPresenterDesktop</a> object.


### -param ppv [out]

Address of a pointer variable that receives the interface pointer identified by <i>riid</i>.


## -returns



If successful, returns the requested interface pointer. Otherwise, returns <b>NULL</b>.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=620314">Complex ink sample</a>



<a href="https://msdn.microsoft.com/7a577536-405b-400d-89bc-c3b3894b448d">IInkDesktopHost</a>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620308">Ink sample</a>



<a href="https://msdn.microsoft.com/3DA4F2D2-5405-42A1-9ED9-3A87BCD84C43">Pen and stylus interactions</a>



<b>Samples</b>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620312">Simple ink sample</a>
 

 


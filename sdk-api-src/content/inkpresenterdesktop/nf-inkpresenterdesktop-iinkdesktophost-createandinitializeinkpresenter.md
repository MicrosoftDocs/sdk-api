---
UID: NF:inkpresenterdesktop.IInkDesktopHost.CreateAndInitializeInkPresenter
title: IInkDesktopHost::CreateAndInitializeInkPresenter method
author: windows-driver-content
description: Creates an IInkPresenterDesktop object on an application thread, connects it to the app's DirectComposition visual tree, and sets the size of the object.
old-location: input_ink\iinkdesktophost_createandinitializeinkpresenter.htm
old-project: input_ink
ms.assetid: 596e1180-04ca-474b-b519-f9ebe468fb6a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CreateAndInitializeInkPresenter method, CreateAndInitializeInkPresenter method, IInkDesktopHost interface, CreateAndInitializeInkPresenter,IInkDesktopHost.CreateAndInitializeInkPresenter, IInkDesktopHost, IInkDesktopHost interface, CreateAndInitializeInkPresenter method, IInkDesktopHost::CreateAndInitializeInkPresenter, InkPresenterDesktop.iinkdesktophost_createandinitializeinkpresenter, inkpresenterdesktop/IInkDesktopHost::CreateAndInitializeInkPresenter, input_ink.iinkdesktophost_createandinitializeinkpresenter
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkPresenterDesktop.h
api_name:
-	IInkDesktopHost.CreateAndInitializeInkPresenter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInkDesktopHost::CreateAndInitializeInkPresenter method


## -description



Creates an <a href="https://msdn.microsoft.com/6d175981-6379-4a61-84b0-8b08274bc3a3">IInkPresenterDesktop</a> object on an application thread, connects it to the app's  <a href="https://msdn.microsoft.com/40e2d02b-77e8-425f-ac5e-3dcddef08173">DirectComposition</a> visual tree, and sets the size of the object.




## -parameters




### -param rootVisual [in]

The <a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a> of the app.


### -param width [in]

The width, in pixels, of the inking area.


### -param height [in]

The height, in pixels, of the inking area.


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
 

 


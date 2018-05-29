---
UID: NF:inkpresenterdesktop.IInkPresenterDesktop.GetSize
title: IInkPresenterDesktop::GetSize
author: windows-sdk-content
description: Gets the size of the InkPresenter object.
old-location: input_ink\iinkpresenterdesktop_getsize.htm
old-project: input_ink
ms.assetid: d4ce0503-72dc-4a25-a48d-58fa50c5047f
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetSize, GetSize method, GetSize method,IInkPresenterDesktop interface, IInkPresenterDesktop interface,GetSize method, IInkPresenterDesktop.GetSize, IInkPresenterDesktop::GetSize, InkPresenterDesktop.iinkpresenterdesktop_getsize, inkpresenterdesktop/IInkPresenterDesktop::GetSize, input_ink.iinkpresenterdesktop_getsize
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkPresenterDesktop.h
api_name:
-	IInkPresenterDesktop.GetSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInkPresenterDesktop::GetSize


## -description


Gets the size of the <a href="https://msdn.microsoft.com/561e2d14-288a-490a-9a3b-5a32e98b51c3">InkPresenter</a> object.


## -parameters




### -param width [out]

The width of the object, in DIPs.


### -param height [out]

The height of the object, in DIPs.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=620314">Complex ink sample</a>



<a href="https://msdn.microsoft.com/6d175981-6379-4a61-84b0-8b08274bc3a3">IInkPresenterDesktop</a>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620308">Ink sample</a>



<a href="https://msdn.microsoft.com/3DA4F2D2-5405-42A1-9ED9-3A87BCD84C43">Pen and stylus interactions</a>



<b>Samples</b>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620312">Simple ink sample</a>
 

 


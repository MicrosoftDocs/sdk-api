---
UID: NF:inkpresenterdesktop.IInkPresenterDesktop.SetCommitRequestHandler
title: IInkPresenterDesktop::SetCommitRequestHandler
author: windows-sdk-content
description: Sets an IInkCommitRequestHandler object that enables the app (instead of an IInkPresenterDesktop object) to commit all pending Microsoft DirectComposition commands to the app's DirectComposition visual tree.
old-location: input_ink\iinkpresenterdesktop_setcommitrequesthandler.htm
old-project: input_ink
ms.assetid: b53eba5d-c53d-45a4-ae51-5a8a27043554
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: IInkPresenterDesktop interface,SetCommitRequestHandler method, IInkPresenterDesktop.SetCommitRequestHandler, IInkPresenterDesktop::SetCommitRequestHandler, InkPresenterDesktop.iinkpresenterdesktop_setcommitrequesthandler, SetCommitRequestHandler, SetCommitRequestHandler method, SetCommitRequestHandler method,IInkPresenterDesktop interface, inkpresenterdesktop/IInkPresenterDesktop::SetCommitRequestHandler, input_ink.iinkpresenterdesktop_setcommitrequesthandler
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
 - IInkPresenterDesktop.SetCommitRequestHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInkPresenterDesktop::SetCommitRequestHandler


## -description


Sets an <a href="https://msdn.microsoft.com/ac6952b5-e2c7-4266-86c0-8e74b879f61c">IInkCommitRequestHandler</a> object that enables the app (instead of an <a href="https://msdn.microsoft.com/6d175981-6379-4a61-84b0-8b08274bc3a3">IInkPresenterDesktop</a> object) to  commit all pending    Microsoft DirectComposition commands to the app's  <a href="https://msdn.microsoft.com/40e2d02b-77e8-425f-ac5e-3dcddef08173">DirectComposition</a> visual tree. 

This supports a custom drying mode and synchronizes the transition of "wet" ink from the <a href="https://msdn.microsoft.com/6d175981-6379-4a61-84b0-8b08274bc3a3">IInkPresenterDesktop</a> object to "dry" ink in the app's  <a href="https://msdn.microsoft.com/40e2d02b-77e8-425f-ac5e-3dcddef08173">DirectComposition</a> visual tree.


## -parameters




### -param handler [in]

The <a href="https://msdn.microsoft.com/ac6952b5-e2c7-4266-86c0-8e74b879f61c">IInkCommitRequestHandler</a> that processes the ink input.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?LinkID=620314">Complex ink sample</a>



<a href="https://msdn.microsoft.com/6d175981-6379-4a61-84b0-8b08274bc3a3">IInkPresenterDesktop</a>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620308">Ink sample</a>



<a href="https://msdn.microsoft.com/3DA4F2D2-5405-42A1-9ED9-3A87BCD84C43">Pen and stylus interactions</a>



<b>Samples</b>



<a href="http://go.microsoft.com/fwlink/p/?LinkID=620312">Simple ink sample</a>
 

 


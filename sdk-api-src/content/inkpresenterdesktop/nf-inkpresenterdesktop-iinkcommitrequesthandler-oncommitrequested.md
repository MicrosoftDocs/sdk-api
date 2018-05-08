---
UID: NF:inkpresenterdesktop.IInkCommitRequestHandler.OnCommitRequested
title: IInkCommitRequestHandler::OnCommitRequested
author: windows-driver-content
description: Requests that the app commit all pending Microsoft DirectComposition commands to the app's DirectComposition visual tree.
old-location: input_ink\iinkcommitrequesthandler_oncommitrequested.htm
old-project: input_ink
ms.assetid: c40ddcd3-ebb6-442b-b36d-2d7d27cfa5db
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IInkCommitRequestHandler interface,OnCommitRequested method, IInkCommitRequestHandler.OnCommitRequested, IInkCommitRequestHandler::OnCommitRequested, InkPresenterDesktop.iinkcommitrequesthandler_oncommitrequested, OnCommitRequested, OnCommitRequested method, OnCommitRequested method,IInkCommitRequestHandler interface, inkpresenterdesktop/IInkCommitRequestHandler::OnCommitRequested, input_ink.iinkcommitrequesthandler_oncommitrequested
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
-	IInkCommitRequestHandler.OnCommitRequested
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInkCommitRequestHandler::OnCommitRequested


## -description


Requests that the app commit all pending    Microsoft DirectComposition commands to the app's  <a href="https://msdn.microsoft.com/40e2d02b-77e8-425f-ac5e-3dcddef08173">DirectComposition</a> visual tree. 


## -parameters






## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ac6952b5-e2c7-4266-86c0-8e74b879f61c">IInkCommitRequestHandler</a>



<a href="https://msdn.microsoft.com/3DA4F2D2-5405-42A1-9ED9-3A87BCD84C43">Pen and stylus interactions</a>
 

 


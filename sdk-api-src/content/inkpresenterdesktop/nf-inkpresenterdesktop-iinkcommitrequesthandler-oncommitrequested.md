---
UID: NF:inkpresenterdesktop.IInkCommitRequestHandler.OnCommitRequested
title: IInkCommitRequestHandler::OnCommitRequested (inkpresenterdesktop.h)
description: Requests that the app commit all pending Microsoft DirectComposition commands to the app's DirectComposition visual tree.
helpviewer_keywords: ["IInkCommitRequestHandler interface","OnCommitRequested method","IInkCommitRequestHandler.OnCommitRequested","IInkCommitRequestHandler::OnCommitRequested","InkPresenterDesktop.iinkcommitrequesthandler_oncommitrequested","OnCommitRequested","OnCommitRequested method","OnCommitRequested method","IInkCommitRequestHandler interface","inkpresenterdesktop/IInkCommitRequestHandler::OnCommitRequested","input_ink.iinkcommitrequesthandler_oncommitrequested"]
old-location: input_ink\iinkcommitrequesthandler_oncommitrequested.htm
tech.root: input_ink
ms.assetid: c40ddcd3-ebb6-442b-b36d-2d7d27cfa5db
ms.date: 12/05/2018
ms.keywords: IInkCommitRequestHandler interface,OnCommitRequested method, IInkCommitRequestHandler.OnCommitRequested, IInkCommitRequestHandler::OnCommitRequested, InkPresenterDesktop.iinkcommitrequesthandler_oncommitrequested, OnCommitRequested, OnCommitRequested method, OnCommitRequested method,IInkCommitRequestHandler interface, inkpresenterdesktop/IInkCommitRequestHandler::OnCommitRequested, input_ink.iinkcommitrequesthandler_oncommitrequested
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkCommitRequestHandler::OnCommitRequested
 - inkpresenterdesktop/IInkCommitRequestHandler::OnCommitRequested
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkPresenterDesktop.h
api_name:
 - IInkCommitRequestHandler.OnCommitRequested
---

# IInkCommitRequestHandler::OnCommitRequested


## -description

Requests that the app commit all pending    Microsoft DirectComposition commands to the app's  <a href="/windows/desktop/directcomp/directcomposition-portal">DirectComposition</a> visual tree.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkcommitrequesthandler">IInkCommitRequestHandler</a>



<a href="/windows/uwp/input-and-devices/pen-and-stylus-interactions">Pen and stylus interactions</a>

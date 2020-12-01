---
UID: NF:inkpresenterdesktop.IInkPresenterDesktop.SetCommitRequestHandler
title: IInkPresenterDesktop::SetCommitRequestHandler (inkpresenterdesktop.h)
description: Sets an IInkCommitRequestHandler object that enables the app (instead of an IInkPresenterDesktop object) to commit all pending Microsoft DirectComposition commands to the app's DirectComposition visual tree.
helpviewer_keywords: ["IInkPresenterDesktop interface","SetCommitRequestHandler method","IInkPresenterDesktop.SetCommitRequestHandler","IInkPresenterDesktop::SetCommitRequestHandler","InkPresenterDesktop.iinkpresenterdesktop_setcommitrequesthandler","SetCommitRequestHandler","SetCommitRequestHandler method","SetCommitRequestHandler method","IInkPresenterDesktop interface","inkpresenterdesktop/IInkPresenterDesktop::SetCommitRequestHandler","input_ink.iinkpresenterdesktop_setcommitrequesthandler"]
old-location: input_ink\iinkpresenterdesktop_setcommitrequesthandler.htm
tech.root: input_ink
ms.assetid: b53eba5d-c53d-45a4-ae51-5a8a27043554
ms.date: 12/05/2018
ms.keywords: IInkPresenterDesktop interface,SetCommitRequestHandler method, IInkPresenterDesktop.SetCommitRequestHandler, IInkPresenterDesktop::SetCommitRequestHandler, InkPresenterDesktop.iinkpresenterdesktop_setcommitrequesthandler, SetCommitRequestHandler, SetCommitRequestHandler method, SetCommitRequestHandler method,IInkPresenterDesktop interface, inkpresenterdesktop/IInkPresenterDesktop::SetCommitRequestHandler, input_ink.iinkpresenterdesktop_setcommitrequesthandler
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
 - IInkPresenterDesktop::SetCommitRequestHandler
 - inkpresenterdesktop/IInkPresenterDesktop::SetCommitRequestHandler
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
 - IInkPresenterDesktop.SetCommitRequestHandler
---

# IInkPresenterDesktop::SetCommitRequestHandler


## -description

Sets an <a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkcommitrequesthandler">IInkCommitRequestHandler</a> object that enables the app (instead of an <a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop">IInkPresenterDesktop</a> object) to  commit all pending    Microsoft DirectComposition commands to the app's  <a href="/windows/desktop/directcomp/directcomposition-portal">DirectComposition</a> visual tree. 

This supports a custom drying mode and synchronizes the transition of "wet" ink from the <a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop">IInkPresenterDesktop</a> object to "dry" ink in the app's  <a href="/windows/desktop/directcomp/directcomposition-portal">DirectComposition</a> visual tree.

## -parameters

### -param handler [in]

The <a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkcommitrequesthandler">IInkCommitRequestHandler</a> that processes the ink input.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk">Complex ink sample</a>



<a href="/previous-versions/windows/desktop/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop">IInkPresenterDesktop</a>






<a href="/windows/uwp/input-and-devices/pen-and-stylus-interactions">Pen and stylus interactions</a>



<b>Samples</b>

<a href="https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/ComplexInk">Complex Ink sample</a>

<a href="https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/SimpleInk">Simple ink sample</a>
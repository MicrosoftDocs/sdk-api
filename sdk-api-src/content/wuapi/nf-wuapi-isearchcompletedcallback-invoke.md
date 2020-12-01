---
UID: NF:wuapi.ISearchCompletedCallback.Invoke
title: ISearchCompletedCallback::Invoke (wuapi.h)
description: Handles the notification of the completion of an asynchronous search that is initiated by calling the IUpdateSearcher.BeginSearch method.
helpviewer_keywords: ["ISearchCompletedCallback interface [Windows Update Agent]","Invoke method","ISearchCompletedCallback.Invoke","ISearchCompletedCallback::Invoke","Invoke","Invoke method [Windows Update Agent]","Invoke method [Windows Update Agent]","ISearchCompletedCallback interface","wua.isearchcompletedcallback_invoke","wuapi/ISearchCompletedCallback::Invoke"]
old-location: wua\isearchcompletedcallback_invoke.htm
tech.root: wua
ms.assetid: 2d06754a-5750-4986-9f54-98f91dcc705b
ms.date: 12/05/2018
ms.keywords: ISearchCompletedCallback interface [Windows Update Agent],Invoke method, ISearchCompletedCallback.Invoke, ISearchCompletedCallback::Invoke, Invoke, Invoke method [Windows Update Agent], Invoke method [Windows Update Agent],ISearchCompletedCallback interface, wua.isearchcompletedcallback_invoke, wuapi/ISearchCompletedCallback::Invoke
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISearchCompletedCallback::Invoke
 - wuapi/ISearchCompletedCallback::Invoke
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - ISearchCompletedCallback.Invoke
---

# ISearchCompletedCallback::Invoke


## -description

Handles the notification of the completion of an asynchronous search that is initiated by calling the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-beginsearch">IUpdateSearcher.BeginSearch</a> method.

## -parameters

### -param searchJob [in]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-isearchjob">ISearchJob</a> interface that contains search information.

### -param callbackArgs [in]

This parameter is reserved for future use and can be ignored. An <a href="/previous-versions/windows/desktop/aa386067(v=vs.85)">ISearchCompletedCallbackArgs</a> interface that contains information on the completion of an asynchronous search.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-isearchcompletedcallback">ISearchCompletedCallback</a>



<a href="/windows/desktop/api/wuapi/nf-wuapi-isearchcompletedcallback-invoke">IUpdateSearcher::BeginSearch</a>
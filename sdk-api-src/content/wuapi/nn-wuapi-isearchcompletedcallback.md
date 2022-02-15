---
UID: NN:wuapi.ISearchCompletedCallback
title: ISearchCompletedCallback (wuapi.h)
description: Contains a method that handles the notification about the completion of an asynchronous search operation.
helpviewer_keywords: ["ISearchCompletedCallback","ISearchCompletedCallback interface [Windows Update Agent]","ISearchCompletedCallback interface [Windows Update Agent]","described","wua.isearchcompletedcallback","wuapi/ISearchCompletedCallback"]
old-location: wua\isearchcompletedcallback.htm
tech.root: wua
ms.assetid: f228808d-7f7e-4107-a4b6-4bac5b48d1b4
ms.date: 12/05/2018
ms.keywords: ISearchCompletedCallback, ISearchCompletedCallback interface [Windows Update Agent], ISearchCompletedCallback interface [Windows Update Agent],described, wua.isearchcompletedcallback, wuapi/ISearchCompletedCallback
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
 - ISearchCompletedCallback
 - wuapi/ISearchCompletedCallback
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
 - ISearchCompletedCallback
---

# ISearchCompletedCallback interface


## -description

Contains a method that handles the notification about the completion of an asynchronous search operation. This interface is implemented by programmers who call the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-beginsearch">IUpdateSearcher.BeginSearch</a> method.

## -inheritance

The <b>ISearchCompletedCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchCompletedCallback</b> also has these types of members:


---
UID: NN:wuapi.ISearchCompletedCallback
title: ISearchCompletedCallback (wuapi.h)
description: Contains a method that handles the notification about the completion of an asynchronous search operation.
old-location: wua\isearchcompletedcallback.htm
tech.root: Wua_Sdk
ms.assetid: f228808d-7f7e-4107-a4b6-4bac5b48d1b4
ms.date: 12/05/2018
ms.keywords: ISearchCompletedCallback, ISearchCompletedCallback interface [Windows Update Agent], ISearchCompletedCallback interface [Windows Update Agent],described, wua.isearchcompletedcallback, wuapi/ISearchCompletedCallback
ms.topic: interface
f1_keywords:
- wuapi/ISearchCompletedCallback
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wuapi.dll
api_name:
- ISearchCompletedCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISearchCompletedCallback interface


## -description


Contains a method that handles the notification about the completion of an asynchronous search operation. This interface is implemented by programmers who call the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-beginsearch">IUpdateSearcher.BeginSearch</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchCompletedCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchCompletedCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchCompletedCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-isearchcompletedcallback-invoke">Invoke</a>
</td>
<td align="left" width="63%">
Handles the notification of the completion of an asynchronous search initiated by calling <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-beginsearch">IUpdateSearcher.BeginSearch</a>


</td>
</tr>
</table> 


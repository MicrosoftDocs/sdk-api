---
UID: NN:wuapi.ISearchJob
title: ISearchJob (wuapi.h)
description: Contains properties and methods that are available to a search operation.
helpviewer_keywords: ["ISearchJob","ISearchJob interface [Windows Update Agent]","ISearchJob interface [Windows Update Agent]","described","wua.isearchjob","wuapi/ISearchJob"]
old-location: wua\isearchjob.htm
tech.root: wua
ms.assetid: aec4a812-cf5d-4986-a776-29c366bb1771
ms.date: 12/05/2018
ms.keywords: ISearchJob, ISearchJob interface [Windows Update Agent], ISearchJob interface [Windows Update Agent],described, wua.isearchjob, wuapi/ISearchJob
f1_keywords:
- wuapi/ISearchJob
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
- ISearchJob
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISearchJob interface


## -description


Contains properties and methods that are available to a search operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchJob</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISearchJob</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ISearchJob</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-isearchjob-cleanup">CleanUp</a>
</td>
<td align="left" width="63%">
Waits for an asynchronous operation to complete and then releases all the callbacks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-isearchjob-requestabort">RequestAbort</a>
</td>
<td align="left" width="63%">
Makes a request to cancel an asynchronous search.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchJob</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-isearchjob-get_asyncstate">AsyncState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the caller-specific state object that is passed to the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-beginsearch">IUpdateSearch.BeginSearch</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-isearchjob-get_iscompleted">IsCompleted</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the call to the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-beginsearch">IUpdateSearch.BeginSearch</a> method is completely processed.

</td>
</tr>
</table> 


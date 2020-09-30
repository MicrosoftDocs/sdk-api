---
UID: NF:wuapi.IUpdateSearcher.BeginSearch
title: IUpdateSearcher::BeginSearch (wuapi.h)
description: Begins execution of an asynchronous search for updates. The search uses the search options that are currently configured.
helpviewer_keywords: ["BeginSearch","BeginSearch method [Windows Update Agent]","BeginSearch method [Windows Update Agent]","IUpdateSearcher interface","IUpdateSearcher interface [Windows Update Agent]","BeginSearch method","IUpdateSearcher.BeginSearch","IUpdateSearcher::BeginSearch","wua.iupdatesearcherbeginsearch","wuapi/IUpdateSearcher::BeginSearch"]
old-location: wua\iupdatesearcherbeginsearch.htm
tech.root: wua
ms.assetid: 8af818b1-7dd8-4f48-b447-5b6dfbfce420
ms.date: 12/05/2018
ms.keywords: BeginSearch, BeginSearch method [Windows Update Agent], BeginSearch method [Windows Update Agent],IUpdateSearcher interface, IUpdateSearcher interface [Windows Update Agent],BeginSearch method, IUpdateSearcher.BeginSearch, IUpdateSearcher::BeginSearch, wua.iupdatesearcherbeginsearch, wuapi/IUpdateSearcher::BeginSearch
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
 - IUpdateSearcher::BeginSearch
 - wuapi/IUpdateSearcher::BeginSearch
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
 - IUpdateSearcher.BeginSearch
---

# IUpdateSearcher::BeginSearch


## -description

Begins execution of an asynchronous search for updates. The search uses the search options that are currently configured.

## -parameters

### -param criteria [in]

A string that specifies the search criteria.

### -param onCompleted [in]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-isearchcompletedcallback">ISearchCompletedCallback</a> interface that is called when an asynchronous search operation is complete.

### -param state [in]

The caller-specific  state that is returned by the <a href="/windows/desktop/api/wuapi/nf-wuapi-isearchjob-get_asyncstate">AsyncState</a> property of the <a href="/windows/desktop/api/wuapi/nn-wuapi-isearchjob">ISearchJob</a> interface.

### -param retval [out]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-isearchjob">ISearchJob</a> interface that represents the current operation that might be pending. 

The caller passes the returned value to the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-endsearch">EndSearch</a> method to complete a search operation.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter value is invalid or <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This  method cannot be called from a remote computer.

</td>
</tr>
</table>

## -remarks

For a complete description of search criteria syntax, see <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-search">Search</a>.

  As an alternative to implementing the <a href="/windows/desktop/api/wuapi/nn-wuapi-isearchcompletedcallback">ISearchCompletedCallback</a> interface, you can use a script to   implement a callback routine of any identifier with DISPID 0 on an automation object. The type of the <i>onCompleted</i> parameter is <b>IUnknown*</b>.

When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="/windows/desktop/Wua_Sdk/guidelines-for-asynchronous-wua-operations">Guidelines for Asynchronous WUA Operations</a>.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a>
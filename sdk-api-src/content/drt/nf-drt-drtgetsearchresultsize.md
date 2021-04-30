---
UID: NF:drt.DrtGetSearchResultSize
title: DrtGetSearchResultSize function (drt.h)
description: DrtGetSearchResultSize function returns the size of the next available search result.
helpviewer_keywords: ["DrtGetSearchResultSize","DrtGetSearchResultSize function [Peer Networking]","drt/DrtGetSearchResultSize","p2p.drtgetsearchresultsize"]
old-location: p2p\drtgetsearchresultsize.htm
tech.root: p2p
ms.assetid: ef17c42e-4cf9-4b5c-b6ef-430500fddff2
ms.date: 12/05/2018
ms.keywords: DrtGetSearchResultSize, DrtGetSearchResultSize function [Peer Networking], drt/DrtGetSearchResultSize, p2p.drtgetsearchresultsize
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Drt.lib
req.dll: Drt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrtGetSearchResultSize
 - drt/DrtGetSearchResultSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtGetSearchResultSize
---

# DrtGetSearchResultSize function


## -description

The <b>DrtGetSearchResultSize</b> function returns the size of the next available search result.

## -parameters

### -param hSearchContext [in]

Handle to the search context to close. This parameter is returned by the <a href="/windows/desktop/api/drt/nf-drt-drtstartsearch">DrtStartSearch</a> function.

### -param pulSearchResultSize [out]

Holds the size of the next available search result.

## -returns

Returns S_OK if the function succeeds. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pulSearchResultSize</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>hSearchContext</i> is an invalid handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_FAULTED</b></dt>
</dl>
</td>
<td width="60%">
The DRT cloud is in the faulted state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_NO_MORE</b></dt>
</dl>
</td>
<td width="60%">
There are no more results to return.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The search failed because it timed out. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_SEARCH_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The search is still in progress.

</td>
</tr>
</table>

## -remarks

The application will receive S_OK and continue to loop using the <b>DrtGetSearchResultSize</b> and <a href="/windows/desktop/api/drt/nf-drt-drtgetsearchresult">DrtGetSearchResult</a> functions as long as the queue contains the search results. When the queue is empty the <b>DrtGetSearchResult</b> function will return DRT_E_SEARCH_IN_PROGRESS or DRT_E_NO_MORE.

## -see-also

<a href="/windows/desktop/api/drt/nf-drt-drtstartsearch">DrtStartSearch</a>
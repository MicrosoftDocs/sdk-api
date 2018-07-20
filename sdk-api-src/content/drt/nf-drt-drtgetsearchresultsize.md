---
UID: NF:drt.DrtGetSearchResultSize
title: DrtGetSearchResultSize function
author: windows-sdk-content
description: DrtGetSearchResultSize function returns the size of the next available search result.
old-location: p2p\drtgetsearchresultsize.htm
old-project: p2psdk
ms.assetid: ef17c42e-4cf9-4b5c-b6ef-430500fddff2
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: DrtGetSearchResultSize, DrtGetSearchResultSize function [Peer Networking], drt/DrtGetSearchResultSize, p2p.drtgetsearchresultsize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: DRT_REGISTRATION_STATE, *PDRT_REGISTRATION_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtGetSearchResultSize
product: Windows
targetos: Windows
req.lib: Drt.lib
req.dll: Drt.dll
req.irql: 
---

# DrtGetSearchResultSize function


## -description


The <b>DrtGetSearchResultSize</b> function returns the size of the next available search result.


## -parameters




### -param hSearchContext [in]

Handle to the search context to close. This parameter is returned by the <a href="https://msdn.microsoft.com/d43634d5-eb0a-4f84-9248-977c544db984">DrtStartSearch</a> function.


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



The application will receive S_OK and continue to loop using the <b>DrtGetSearchResultSize</b> and <a href="https://msdn.microsoft.com/b89ea470-072e-46b6-9f5d-3e05aa012188">DrtGetSearchResult</a> functions as long as the queue contains the search results. When the queue is empty the <b>DrtGetSearchResult</b> function will return DRT_E_SEARCH_IN_PROGRESS or DRT_E_NO_MORE.




## -see-also




<a href="https://msdn.microsoft.com/d43634d5-eb0a-4f84-9248-977c544db984">DrtStartSearch</a>
 

 


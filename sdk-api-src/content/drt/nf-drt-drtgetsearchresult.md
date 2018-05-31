---
UID: NF:drt.DrtGetSearchResult
title: DrtGetSearchResult function
author: windows-sdk-content
description: DrtGetSearchResult function.
old-location: p2p\drtgetsearchresult.htm
old-project: P2PSdk
ms.assetid: b89ea470-072e-46b6-9f5d-3e05aa012188
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: DrtGetSearchResult, DrtGetSearchResult function [Peer Networking], drt/DrtGetSearchResult, p2p.drtgetsearchresult
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
req.typenames: DRT_REGISTRATION_STATE, *PDRT_REGISTRATION_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	drt.dll
api_name:
-	DrtGetSearchResult
product: Windows
targetos: Windows
req.lib: Drt.lib
req.dll: Drt.dll
req.irql: 
---

# DrtGetSearchResult function


## -description


The <b>DrtGetSearchResult</b> function allows the caller to retrieve the search result(s).


## -parameters




### -param hSearchContext [in]

Handle to the search context to close. This parameter is returned by the <a href="https://msdn.microsoft.com/d43634d5-eb0a-4f84-9248-977c544db984">DrtStartSearch</a> function.


### -param ulSearchResultSize

TBD


### -param pSearchResult

TBD




#### - ppSearchResult [out]

Pointer to the <a href="https://msdn.microsoft.com/23cf713e-2730-456c-a3da-649c5ed00ffb">DRT_SEARCH_RESULT</a> structure containing the search result.


## -returns



This function returns S_OK on success. Other possible values include:

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
<i>ulSearchPathSize</i>  is less than the  size of <a href="https://msdn.microsoft.com/23cf713e-2730-456c-a3da-649c5ed00ffb">DRT_SEARCH_RESULT</a>.

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
the DRT cloud is in the faulted state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The provided buffer is insufficient in size to contain the search result.

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
The search is currently in progress.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d43634d5-eb0a-4f84-9248-977c544db984">DrtStartSearch</a>
 

 


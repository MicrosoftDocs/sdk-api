---
UID: NF:drt.DrtEndSearch
title: DrtEndSearch function (drt.h)
author: windows-sdk-content
description: DrtEndSearch function cancels a search for a key in a DRT.
old-location: p2p\drtendsearch.htm
tech.root: P2PSdk
ms.assetid: 1a99476f-69ee-4aeb-8c9b-e06315ec095d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrtEndSearch, DrtEndSearch function [Peer Networking], drt/DrtEndSearch, p2p.drtendsearch
ms.topic: function
f1_keywords: 
 - "drt/DrtEndSearch"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtEndSearch
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DrtEndSearch function


## -description


The <b>DrtEndSearch</b> function cancels a search for a key in a DRT.  This API can be called at any point after a search is issued. 


## -parameters




### -param hSearchContext [in]

Handle to the search context to end. This parameter is returned from <a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtstartsearch">DrtStartSearch</a>.


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
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hSearchContext</i> handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The DRT infrastructure is unaware of the requested search.

</td>
</tr>
</table>
 




## -remarks



Calling the <b>DrtEndSearch</b> function will stop the return of search results via <a href="https://docs.microsoft.com/windows/desktop/api/drt/ns-drt-drt_search_result">DRT_SEARCH_RESULT</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/drt/ns-drt-drt_search_result">DRT_SEARCH_RESULT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtcontinuesearch">DrtContinueSearch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/drt/nf-drt-drtstartsearch">DrtStartSearch</a>
 

 


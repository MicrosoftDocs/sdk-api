---
UID: NF:drt.DrtContinueSearch
title: DrtContinueSearch function (drt.h)
description: DrtContinueSearch function continues an iterative search for a key.
helpviewer_keywords: ["DrtContinueSearch","DrtContinueSearch function [Peer Networking]","drt/DrtContinueSearch","p2p.drtcontinuesearch"]
old-location: p2p\drtcontinuesearch.htm
tech.root: p2p
ms.assetid: 04bdeb53-4901-41d4-835e-da665095edc5
ms.date: 12/05/2018
ms.keywords: DrtContinueSearch, DrtContinueSearch function [Peer Networking], drt/DrtContinueSearch, p2p.drtcontinuesearch
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
 - DrtContinueSearch
 - drt/DrtContinueSearch
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
 - DrtContinueSearch
---

# DrtContinueSearch function


## -description

The <b>DrtContinueSearch</b> function continues an iterative search for a key.This function is used only when the <b>fIterative</b> flag is set to 'true' in the associated <a href="/windows/desktop/api/drt/ns-drt-drt_search_info">DRT_SEARCH_INFO</a> structure. Call this after getting a <b>DRT_MATCH_INTERMEDIATE</b> search result.

## -parameters

### -param hSearchContext [in]

Handle to the search context  to close. This parameter is returned by the <a href="/windows/desktop/api/drt/nf-drt-drtstartsearch">DrtStartSearch</a> API.

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
This search is not an iterative search.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/drt/ns-drt-drt_search_info">DRT_SEARCH_INFO</a>



<a href="/windows/desktop/api/drt/nf-drt-drtendsearch">DrtEndSearch</a>



<a href="/windows/desktop/api/drt/nf-drt-drtstartsearch">DrtStartSearch</a>
---
UID: NF:drt.DrtStartSearch
title: DrtStartSearch function (drt.h)
description: The DrtStartSearch function searches the DRT for a key using criteria specified in the DRT_SEARCH_INFO structure.
helpviewer_keywords: ["DrtStartSearch","DrtStartSearch function [Peer Networking]","drt/DrtStartSearch","p2p.drtstartsearch"]
old-location: p2p\drtstartsearch.htm
tech.root: p2p
ms.assetid: d43634d5-eb0a-4f84-9248-977c544db984
ms.date: 12/05/2018
ms.keywords: DrtStartSearch, DrtStartSearch function [Peer Networking], drt/DrtStartSearch, p2p.drtstartsearch
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
 - DrtStartSearch
 - drt/DrtStartSearch
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
 - DrtStartSearch
---

# DrtStartSearch function


## -description

The <b>DrtStartSearch</b> function searches the DRT for a key using criteria specified in the <a href="/windows/desktop/api/drt/ns-drt-drt_search_info">DRT_SEARCH_INFO</a> structure.

## -parameters

### -param hDrt [in]

The DRT handle returned by the <a href="/windows/desktop/api/drt/nf-drt-drtopen">DrtOpen</a> function.

### -param pKey [in]

Pointer to the <a href="/windows/desktop/api/drt/ns-drt-drt_data">DRT_DATA</a> structure containing the key.

### -param pInfo [in, optional]

Pointer to the <a href="/windows/desktop/api/drt/ns-drt-drt_search_info">DRT_SEARCH_INFO</a> structure that specifies the properties of the search.

### -param timeout

Specifies the milliseconds until the search is stopped.

### -param hEvent [in]

Handle to the event that is signaled when the <b>DrtStartSearch</b> API finishes or an intermediate node is found.

### -param pvContext [in, optional]

Pointer to the context data passed to the application through the event.

### -param hSearchContext [out]

Handle used in the call to <a href="/windows/desktop/api/drt/nf-drt-drtendsearch">DrtEndSearch</a>.

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
hDrt is an invalid handle or phKeyRegistration is an invalid handle

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<ul>
<li><i>hSearchContext</i> is <b>NULL</b>.</li>
<li><i>pKey</i> is <b>NULL</b></li>
<li>The <b>pb</b> member of  the <a href="/windows/desktop/api/drt/ns-drt-drt_data">DRT_DATA</a> structure of <i>pKey</i> is <b>NULL</b>.</li>
<li><i>pInfo</i> was passed in, the minimum key is set inside <i>pInfo</i> for range search, but the maximum key is <b>NULL</b>.</li>
<li><i>pInfo</i> was passed in, the maximum key is set inside <i>pInfo</i> for range search, but the minimum key is <b>NULL</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_KEY_SIZE</b></dt>
</dl>
</td>
<td width="60%">
<ul>
<li>The <b>cb</b> member of  the <a href="/windows/desktop/api/drt/ns-drt-drt_data">DRT_DATA</a> structure of <i>pKey</i> is not equal to 256 bits.</li>
<li><i>pInfo</i> was passed in, but the key size of the minimum key set inside <i>pInfo</i> is not equal to 256 bits.</li>
<li><i>pInfo</i> was passed in, but the key size of the maximum key set inside <i>pInfo</i> is not equal to 256 bits.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_SEARCH_INFO</b></dt>
</dl>
</td>
<td width="60%">
<i>pInfo</i> was passed in but the <b>dwSize</b> of <i>pInfo</i> is not equal to size of the <a href="/windows/desktop/api/drt/ns-drt-drt_search_info">DRT_SEARCH_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_MAX_ENDPOINTS</b></dt>
</dl>
</td>
<td width="60%">
<i>pInfo</i> was passed in but max endpoints (<b>cMaxEndpoints</b>) is set to 0 inside <i>pInfo</i> or
<i>pInfo</i> was passed in but <b>cMaxEndpoints</b> is greater than 1 with <b>fAnyMatchInRange</b> set to <b>TRUE</b>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_SEARCH_RANGE</b></dt>
</dl>
</td>
<td width="60%">
Min and max key values are equal, but target is different.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The DRT is shutting down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unexpected fatal error has occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/drt/ns-drt-drt_search_info">DRT_SEARCH_INFO</a>



<a href="/windows/desktop/api/drt/nf-drt-drtcontinuesearch">DrtContinueSearch</a>



<a href="/windows/desktop/api/drt/nf-drt-drtendsearch">DrtEndSearch</a>



<a href="/windows/desktop/api/drt/nf-drt-drtopen">DrtOpen</a>
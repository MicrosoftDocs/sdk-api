---
UID: NF:ntquery.CIState
title: CIState function (ntquery.h)
description: Queries the state of the selected catalog.
helpviewer_keywords: ["CIState","CIState function [Indexing Service]","_idxs_CIState","indexsrv.cistate","ntquery/CIState"]
old-location: indexsrv\cistate.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_9syt.htm
ms.date: 12/05/2018
ms.keywords: CIState, CIState function [Indexing Service], _idxs_CIState, indexsrv.cistate, ntquery/CIState
f1_keywords:
- ntquery/CIState
dev_langs:
- c++
req.header: ntquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntquery.lib
req.dll: Ntquery.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ntquery.dll
api_name:
- CIState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CIState function


## -description


> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

Queries the state of the selected catalog.


## -parameters




### -param pwcsCat [in]

The catalog name, such as L"Web" or L"system".


### -param pwcsMachine [in]

The computer name on which the catalog is located, such as "." for the local computer or "RemoteServer1".


### -param pCiState [out]

A pointer to a <a href="/windows/desktop/api/ntquery/ns-ntquery-ci_state">CI_STATE</a> structure that receives the catalog state.


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pwcsCat</i> or <i>pCiState</i> is not a valid pointer, or the structure to which <i>pCiState</i> points is not large enough to hold the resulting state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CI_E_NO_CATALOG</b></dt>
</dl>
</td>
<td width="60%">
This function failed because the catalog was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CI_E_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The function failed because Indexing Service is not running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The function failed because Indexing Service is too busy to respond to the query.

</td>
</tr>
</table>
 




## -remarks



The <a href="/windows/desktop/api/ntquery/ns-ntquery-ci_state">CI_STATE</a> structure must be initialized (the <b>cbStruct</b> member must be correctly set) before calling the <b>CIState</b> function.




## -see-also




<a href="/windows/desktop/api/ntquery/ns-ntquery-ci_state">CI_STATE</a>
 

 
---
UID: NF:ntquery.SetCatalogState
title: SetCatalogState function (ntquery.h)
description: Sets the catalog state for backup or other purposes.
helpviewer_keywords: ["SetCatalogState","SetCatalogState function [Indexing Service]","_idxs_SetCatalogState","indexsrv.setcatalogstate","ntquery/SetCatalogState"]
old-location: indexsrv\setcatalogstate.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_809x.htm
ms.date: 12/05/2018
ms.keywords: SetCatalogState, SetCatalogState function [Indexing Service], _idxs_SetCatalogState, indexsrv.setcatalogstate, ntquery/SetCatalogState
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetCatalogState
 - ntquery/SetCatalogState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntquery.dll
api_name:
 - SetCatalogState
---

# SetCatalogState function


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

Sets the catalog state for backup or other purposes.

## -parameters

### -param pwcsCat

A pointer to the name of the catalog, for example, L"system" or L"Web".

### -param pwcsMachine

A pointer to the name of the computer where the catalog exists; for example, L"." for the local computer.

### -param dwNewState

The state of the catalog. See <a href="/previous-versions/windows/desktop/indexsrv/cicat-constants">CICAT_* Constants</a>.

### -param pdwOldState

A pointer to a value that receives one of the CICAT_* constants that reflects the current state of the catalog.

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
The function received an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CI_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The function failed because either the catalog or the computer was not found.

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
The function failed because Indexing Service is too busy.

</td>
</tr>
</table>

## -remarks

A catalog can be read-only if any of the following conditions exist:

<ul>
<li>The value of the <b>HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\ContentIndex\Catalogs\&lt;catalog name&gt;\IsReadOnly</b> registry entry is set to 1. </li>
<li>The catalog is on a write-protected volume.</li>
<li>The catalog, specifically the file cicat.hsh, is read-only.</li>
</ul>


If any of the preceding conditions exist and the CICAT_WRITABLE bit is set, it does not have the desired effect and the catalog is opened read-only.

If the <i>dwNewState</i> parameter contains CICAT_NO_QUERY, the system checks to see whether the catalog can be set to a writable state. If any of the preceding conditions exist that prevent the catalog from being writable, the catalog remains read-only and the <i>pdwOldState</i> parameter returns CICAT_READONLY. However, because the intention of the flag is to halt querying, the catalog stops accepting queries even though it is in this read-only state.

Specifically, if you make the call:



<code>SetCatalogState("System", ".", CICAT_NO_QUERY, &amp;OldState);</code>

the value of the <i>pdwOldState</i> parameter on return will contain CICAT_NO_QUERY in addition to CI_CAT_WRITABLE or CI_CAT_READONLY values, depending on the READONLY/WRITABLE attributes of the volume or file.

If you make the call to <b>SetCatalogState</b>, where the <i>dwNewState</i> parameter is any value other than CICAT_NO_QUERY, then the value of the *<i>pdwOldState</i> parameter on return will contain one of the mutually exclusive CICAT_* constants (excluding CICAT_NO_QUERY and CICAT_GET_STATE) which reflects the current state of the catalog.

<div class="alert"><b>Note</b>  If you issue a <b>net pause</b> command or a <b>net continue</b> command for Indexing Service, the state changes that were set by the <b>SetCatalogState</b> function are not preserved.</div>
<div> </div>
For examples of changes in a catalog's state, see the ChgState sample in the Platform SDK directory mssdk\samples\winbase\indexing\chgstate.

## -see-also

<a href="/previous-versions/windows/desktop/indexsrv/locating-the-catalog-for-the-selected-scope">LocateCatalogs</a>
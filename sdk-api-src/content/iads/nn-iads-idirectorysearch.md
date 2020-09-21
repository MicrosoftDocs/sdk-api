---
UID: NN:iads.IDirectorySearch
title: IDirectorySearch (iads.h)
description: The IDirectorySearch interface is a pure COM interface that provides a low overhead method that non-Automation clients can use to perform queries in the underlying directory.
helpviewer_keywords: ["IDirectorySearch","IDirectorySearch interface [ADSI]","IDirectorySearch interface [ADSI]","described","_ds_idirectorysearch","adsi.idirectorysearch","iads/IDirectorySearch"]
old-location: adsi\idirectorysearch.htm
tech.root: adsi
ms.assetid: e8989795-8f72-476a-a69e-c0e8800289ab
ms.date: 12/05/2018
ms.keywords: IDirectorySearch, IDirectorySearch interface [ADSI], IDirectorySearch interface [ADSI],described, _ds_idirectorysearch, adsi.idirectorysearch, iads/IDirectorySearch
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Activeds.dll; Adsldp.dll; Adsldpc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectorySearch
 - iads/IDirectorySearch
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
 - Adsldp.dll
 - Adsldpc.dll
api_name:
 - IDirectorySearch
---

# IDirectorySearch interface


## -description

The <b>IDirectorySearch</b> interface is a pure COM interface that provides a low overhead method that non-Automation clients can use to perform queries in the underlying directory.

Of the ADSI system-supplied providers, only the LDAP provider supports this interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectorySearch</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectorySearch</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectorySearch</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-abandonsearch">AbandonSearch</a>
</td>
<td align="left" width="63%">
Abandons a search already in process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-closesearchhandle">CloseSearchHandle</a>
</td>
<td align="left" width="63%">
Releases the search result from memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch">ExecuteSearch</a>
</td>
<td align="left" width="63%">
Executes an individual search.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-freecolumn">FreeColumn</a>
</td>
<td align="left" width="63%">
Frees the  <a href="/windows/desktop/api/iads/ns-iads-ads_search_column">ADS_SEARCH_COLUMN</a> structure created by the  <a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn">GetColumn</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn">GetColumn</a>
</td>
<td align="left" width="63%">
Gets the item in a specified column from the current row of the search result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getfirstrow">GetFirstRow</a>
</td>
<td align="left" width="63%">
Gets the first row of the search result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextcolumnname">GetNextColumnName</a>
</td>
<td align="left" width="63%">
Gets the name of the next column of the search result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextrow">GetNextRow</a>
</td>
<td align="left" width="63%">
Gets the next row of the search result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-getpreviousrow">GetPreviousRow</a>
</td>
<td align="left" width="63%">
Gets the previous row of the search result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference">SetSearchPreference</a>
</td>
<td align="left" width="63%">
Sets options for conducting a search.

</td>
</tr>
</table>
---
UID: NF:ntquery.LoadIFilter
title: LoadIFilter function (ntquery.h)
description: Retrieves IFilter from path name for object.
helpviewer_keywords: ["LoadIFilter","LoadIFilter function [Indexing Service]","_idxs_LoadIFilter","indexsrv.loadifilter","ntquery/LoadIFilter"]
old-location: indexsrv\loadifilter.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_5ar6.htm
ms.date: 12/05/2018
ms.keywords: LoadIFilter, LoadIFilter function [Indexing Service], _idxs_LoadIFilter, indexsrv.loadifilter, ntquery/LoadIFilter
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
req.dll: Query.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LoadIFilter
 - ntquery/LoadIFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Query.dll
 - NtQuery.dll
api_name:
 - LoadIFilter
---

# LoadIFilter function


## -description

<p class="CCE_Message">[Indexing Service is unsupported as of Windows XP. Instead, use <a href="/windows/desktop/search/-search-3x-wds-overview">Windows Search</a> for client side search and  <a href="https://www.microsoft.com/download/details.aspx?id=18914">Microsoft Search Server Express</a> for server side search.]

Retrieves <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> from path name for object.

## -parameters

### -param pwcsPath

A pointer to the full path of an object for which an <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> interface pointer is to be returned. The path can include a full filename or only the file name extension; for example, ".ext".

### -param pUnkOuter [in]

A pointer to the controlling <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the aggregate in which this storage object exists.

### -param ppIUnk [out]

A pointer to a variable that receives the <a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> interface pointer.

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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The function was denied access to the filter file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The function encountered an invalid handle, probably due to a low-memory situation.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function did not have sufficient memory or other resources to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unknown error has occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ntquery/nf-ntquery-bindifilterfromstorage">BindIFilterFromStorage</a>



<a href="/windows/desktop/api/ntquery/nf-ntquery-bindifilterfromstream">BindIFilterFromStream</a>



<a href="/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a>
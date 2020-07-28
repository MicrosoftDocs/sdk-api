---
UID: NF:ntquery.BindIFilterFromStream
title: BindIFilterFromStream function (ntquery.h)
description: Retrieves the IFilter interface pointer for the specified storage object. This is especially useful when filtering the contents of a document and processing embedded OLE objects accessible through their IStream interfaces.
helpviewer_keywords: ["BindIFilterFromStream","BindIFilterFromStream function [Indexing Service]","_idxs_BindIFilterFromStream","indexsrv.bindifilterfromstream","ntquery/BindIFilterFromStream"]
old-location: indexsrv\bindifilterfromstream.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_0f8t.htm
ms.date: 12/05/2018
ms.keywords: BindIFilterFromStream, BindIFilterFromStream function [Indexing Service], _idxs_BindIFilterFromStream, indexsrv.bindifilterfromstream, ntquery/BindIFilterFromStream
f1_keywords:
- ntquery/BindIFilterFromStream
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
- BindIFilterFromStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# BindIFilterFromStream function


## -description


<p class="CCE_Message">[Indexing Service is unsupported as of Windows XP. Instead, use <a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-overview">Windows Search</a> for client side search and  <a href="https://www.microsoft.com/download/details.aspx?id=18914">Microsoft Search Server Express</a> for server side search.]

Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> interface pointer for the specified storage object. This is especially useful when filtering the contents of a document and processing embedded OLE objects accessible through their <b>IStream</b> interfaces.



## -parameters




### -param pStm [in]

A pointer to the <b>IStream</b> interface to be used to access the file. 


### -param pUnkOuter [in]

A pointer to the controlling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the aggregate in which this stream object exists.


### -param ppIUnk [out]

A pointer to an output variable that receives the <a href="https://docs.microsoft.com/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a> interface pointer. 


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
The function was denied access to the path of the storage object.

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
 




## -remarks



This function is not a full implementation of a COM persistent handler.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntquery/nf-ntquery-bindifilterfromstorage">BindIFilterFromStorage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntquery/nf-ntquery-loadifilter">LoadIFilter</a>
 

 


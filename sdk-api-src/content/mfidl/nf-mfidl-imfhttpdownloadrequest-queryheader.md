---
UID: NF:mfidl.IMFHttpDownloadRequest.QueryHeader
title: IMFHttpDownloadRequest::QueryHeader (mfidl.h)
description: Invoked by Microsoft Media Foundation to retrieve the values of specified HTTP headers from the response to a previously sent HTTP or HTTPS request.
helpviewer_keywords: ["IMFHttpDownloadRequest interface [Media Foundation]","QueryHeader method","IMFHttpDownloadRequest.QueryHeader","IMFHttpDownloadRequest::QueryHeader","QueryHeader","QueryHeader method [Media Foundation]","QueryHeader method [Media Foundation]","IMFHttpDownloadRequest interface","mf.imfhttpdownloadrequest_queryheader","mfidl/IMFHttpDownloadRequest::QueryHeader"]
old-location: mf\imfhttpdownloadrequest_queryheader.htm
tech.root: mf
ms.assetid: BFAE5257-0BE8-47F3-B3CD-490885E60065
ms.date: 12/05/2018
ms.keywords: IMFHttpDownloadRequest interface [Media Foundation],QueryHeader method, IMFHttpDownloadRequest.QueryHeader, IMFHttpDownloadRequest::QueryHeader, QueryHeader, QueryHeader method [Media Foundation], QueryHeader method [Media Foundation],IMFHttpDownloadRequest interface, mf.imfhttpdownloadrequest_queryheader, mfidl/IMFHttpDownloadRequest::QueryHeader
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFHttpDownloadRequest::QueryHeader
 - mfidl/IMFHttpDownloadRequest::QueryHeader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFHttpDownloadRequest.QueryHeader
---

# IMFHttpDownloadRequest::QueryHeader


## -description

Invoked by Microsoft Media Foundation to retrieve the values of specified HTTP headers from the response to a previously sent HTTP or HTTPS request. Media Foundation invokes this method only after having successfully invoked the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-endreceiveresponse">EndReceiveResponse</a> method.

## -parameters

### -param szHeaderName [in]

The name of the HTTP header for which the value is being queried.

### -param dwIndex [in]

The index number of the specified header, for the case where the response contains multiple headers with the same name. A value of 0 indicates that the value of the first header with the specified name is requested, 1 indicates that the second header is requested, and so on.

### -param ppszHeaderValue [out]

Set to the value of the requested header, not including the carriage return or line feed characters. The memory for <i>ppszHeaderValue</i> must be allocated with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> and will be freed by Media Foundation with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
Successfully returned the value of the specified header with the specified index.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppszHeaderValue</i> parameter is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_OUT_OF_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwIndex</i> parameter value is out of range.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest">IMFHttpDownloadRequest</a>
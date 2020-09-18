---
UID: NF:mfidl.IMFHttpDownloadRequest.GetURL
title: IMFHttpDownloadRequest::GetURL (mfidl.h)
description: Returns the URL that is used for sending the request.
helpviewer_keywords: ["GetURL","GetURL method [Media Foundation]","GetURL method [Media Foundation]","IMFHttpDownloadRequest interface","IMFHttpDownloadRequest interface [Media Foundation]","GetURL method","IMFHttpDownloadRequest.GetURL","IMFHttpDownloadRequest::GetURL","mf.imfhttpdownloadrequest_geturl","mfidl/IMFHttpDownloadRequest::GetURL"]
old-location: mf\imfhttpdownloadrequest_geturl.htm
tech.root: mf
ms.assetid: 38FAD6B8-8C50-492C-BC53-6F301D49083F
ms.date: 12/05/2018
ms.keywords: GetURL, GetURL method [Media Foundation], GetURL method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],GetURL method, IMFHttpDownloadRequest.GetURL, IMFHttpDownloadRequest::GetURL, mf.imfhttpdownloadrequest_geturl, mfidl/IMFHttpDownloadRequest::GetURL
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
 - IMFHttpDownloadRequest::GetURL
 - mfidl/IMFHttpDownloadRequest::GetURL
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
 - IMFHttpDownloadRequest.GetURL
---

# IMFHttpDownloadRequest::GetURL


## -description

Returns the URL that is used for sending the request.

## -parameters

### -param ppszURL [out]

The URL that is used for sending the request to the server. Note that this URL may be different if the server has issued a HTTP protocol “redirect”. The memory for <i>pszURL</i> must be allocated with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>, and will be freed by Media Foundation with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

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
Successfully returned the URL.

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
The <i>ppszURL</i> parameter is an invalid pointer.

</td>
</tr>
</table>

## -remarks

By default, <b>GetURL</b> returns an URL which is synthesized from the parameters provided by Media Foundation in the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsession-setserver">IMFHttpDownloadSession::SetServer</a> and <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsession-createrequest">IMFHttpDownloadSession::CreateRequest</a> methods. However, if the HTTP server has redirected the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest">IMFHttpDownloadRequest</a> to a different server (i.e., through a “302 See Other” HTTP response) then the <b>GetURL</b> method returns the URL that the HTTP server specified.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest">IMFHttpDownloadRequest</a>
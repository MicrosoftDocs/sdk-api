---
UID: NF:mfidl.IMFHttpDownloadRequest.AddHeader
title: IMFHttpDownloadRequest::AddHeader (mfidl.h)
description: Invoked by Microsoft Media Foundation to add a single HTTP header to a HTTP request. Microsoft Media Foundation will invoke this method once for each header that shall be included in the HTTP request, before it invokes the BeginSendRequest method.
helpviewer_keywords: ["AddHeader","AddHeader method [Media Foundation]","AddHeader method [Media Foundation]","IMFHttpDownloadRequest interface","IMFHttpDownloadRequest interface [Media Foundation]","AddHeader method","IMFHttpDownloadRequest.AddHeader","IMFHttpDownloadRequest::AddHeader","mf.imfhttpdownloadrequest_addheader","mfidl/IMFHttpDownloadRequest::AddHeader"]
old-location: mf\imfhttpdownloadrequest_addheader.htm
tech.root: mf
ms.assetid: 37A2C9D8-EFF6-49D5-B495-EDBEEABD59CE
ms.date: 12/05/2018
ms.keywords: AddHeader, AddHeader method [Media Foundation], AddHeader method [Media Foundation],IMFHttpDownloadRequest interface, IMFHttpDownloadRequest interface [Media Foundation],AddHeader method, IMFHttpDownloadRequest.AddHeader, IMFHttpDownloadRequest::AddHeader, mf.imfhttpdownloadrequest_addheader, mfidl/IMFHttpDownloadRequest::AddHeader
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
 - IMFHttpDownloadRequest::AddHeader
 - mfidl/IMFHttpDownloadRequest::AddHeader
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
 - IMFHttpDownloadRequest.AddHeader
---

# IMFHttpDownloadRequest::AddHeader


## -description

Invoked by Microsoft Media Foundation to add a single HTTP header to a HTTP request.  Microsoft Media Foundation will invoke this method once for each header that shall be included in the HTTP request, before it invokes the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadrequest-beginsendrequest">BeginSendRequest</a> method.

## -parameters

### -param szHeader [in]

Contains a single HTTP request header, for example, “Accept: */*”. The string does not include the carriage return or line feed characters.

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
Successfully added the header to the list of headers to be sent with the request.

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
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest">IMFHttpDownloadRequest</a>
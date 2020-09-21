---
UID: NF:mfidl.IMFHttpDownloadSessionProvider.CreateHttpDownloadSession
title: IMFHttpDownloadSessionProvider::CreateHttpDownloadSession (mfidl.h)
description: Called by the Microsoft Media Foundation to open HTTP or HTTPS URLs instead of using the default implementation.
helpviewer_keywords: ["CreateHttpDownloadSession","CreateHttpDownloadSession method [Media Foundation]","CreateHttpDownloadSession method [Media Foundation]","IMFHttpDownloadSessionProvider interface","IMFHttpDownloadSessionProvider interface [Media Foundation]","CreateHttpDownloadSession method","IMFHttpDownloadSessionProvider.CreateHttpDownloadSession","IMFHttpDownloadSessionProvider::CreateHttpDownloadSession","mf.imfhttpdownloadsessionprovider_createhttpdownloadsession","mfidl/IMFHttpDownloadSessionProvider::CreateHttpDownloadSession"]
old-location: mf\imfhttpdownloadsessionprovider_createhttpdownloadsession.htm
tech.root: mf
ms.assetid: D9DAE789-1C0E-42B4-87B6-593D3B67FE1F
ms.date: 12/05/2018
ms.keywords: CreateHttpDownloadSession, CreateHttpDownloadSession method [Media Foundation], CreateHttpDownloadSession method [Media Foundation],IMFHttpDownloadSessionProvider interface, IMFHttpDownloadSessionProvider interface [Media Foundation],CreateHttpDownloadSession method, IMFHttpDownloadSessionProvider.CreateHttpDownloadSession, IMFHttpDownloadSessionProvider::CreateHttpDownloadSession, mf.imfhttpdownloadsessionprovider_createhttpdownloadsession, mfidl/IMFHttpDownloadSessionProvider::CreateHttpDownloadSession
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
 - IMFHttpDownloadSessionProvider::CreateHttpDownloadSession
 - mfidl/IMFHttpDownloadSessionProvider::CreateHttpDownloadSession
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
 - IMFHttpDownloadSessionProvider.CreateHttpDownloadSession
---

# IMFHttpDownloadSessionProvider::CreateHttpDownloadSession


## -description

Called by the Microsoft Media Foundation to open HTTP or HTTPS URLs instead of using the default implementation.

## -parameters

### -param wszScheme [in]

The name of the protocol to for which an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession">IMFHttpDownloadSession</a> is being requested.  Microsoft Media Foundation specifies the protocol scheme of the URL that the application provided the Media Foundation Source Resolver. Valid values include “http” for HTTP, and “https” for HTTPS. URL scheme names are generally not case-sensitive.

### -param ppDownloadSession [out]

On successful execution, the parameter is set to a pointer to an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession">IMFHttpDownloadSession</a> interface. The returned interface is used by Microsoft Media Foundation to open a single HTTP or HTTPS URL.

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
Successfully created the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession">IMFHttpDownloadSession</a> object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value specified for the <i>wszScheme</i> parameter is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppDownloadSession</i> parameter is an invalid pointer.

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

## -remarks

Specifying “https” as the value of <i>wszScheme</i> does not imply that HTTPS will be used for a particular request, as that is specified on a per-request basis in <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsession-createrequest">IMFhttpDownloadSession::CreateRequest</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsessionprovider">IMFHttpDownloadSessionProvider</a>
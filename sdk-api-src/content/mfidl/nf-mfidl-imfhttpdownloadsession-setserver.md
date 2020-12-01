---
UID: NF:mfidl.IMFHttpDownloadSession.SetServer
title: IMFHttpDownloadSession::SetServer (mfidl.h)
description: Called by Microsoft Media Foundation to specify parameters common to all requests created by this instance of IMFHttpDownloadSession.
helpviewer_keywords: ["IMFHttpDownloadSession interface [Media Foundation]","SetServer method","IMFHttpDownloadSession.SetServer","IMFHttpDownloadSession::SetServer","SetServer","SetServer method [Media Foundation]","SetServer method [Media Foundation]","IMFHttpDownloadSession interface","mf.imfhttpdownloadsession_setserver","mfidl/IMFHttpDownloadSession::SetServer"]
old-location: mf\imfhttpdownloadsession_setserver.htm
tech.root: mf
ms.assetid: 408D4863-D95F-4BBD-9F0B-9796ED08A256
ms.date: 12/05/2018
ms.keywords: IMFHttpDownloadSession interface [Media Foundation],SetServer method, IMFHttpDownloadSession.SetServer, IMFHttpDownloadSession::SetServer, SetServer, SetServer method [Media Foundation], SetServer method [Media Foundation],IMFHttpDownloadSession interface, mf.imfhttpdownloadsession_setserver, mfidl/IMFHttpDownloadSession::SetServer
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
 - IMFHttpDownloadSession::SetServer
 - mfidl/IMFHttpDownloadSession::SetServer
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
 - IMFHttpDownloadSession.SetServer
---

# IMFHttpDownloadSession::SetServer


## -description

Called  by Microsoft Media Foundation to specify parameters common to all requests created by this instance of <a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession">IMFHttpDownloadSession</a>.

## -parameters

### -param szServerName [in]

The host name, fully qualified DNS name, or IP address of the HTTP server that the requests shall be sent to.

### -param nPort [in]

The TCP port number of the server.

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
Successfully stored the supplied data.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession">IMFHttpDownloadSession</a>
---
UID: NF:upnp.IUPnPServiceAsync.BeginSCPDDownload
title: IUPnPServiceAsync::BeginSCPDDownload (upnp.h)
description: BeginSCPDDownload method initiates the asynchronous download of an Service Control Protocol Description (SCPD) document.
helpviewer_keywords: ["BeginSCPDDownload","BeginSCPDDownload method [UPnP APIs]","BeginSCPDDownload method [UPnP APIs]","IUPnPServiceAsync interface","IUPnPServiceAsync interface [UPnP APIs]","BeginSCPDDownload method","IUPnPServiceAsync.BeginSCPDDownload","IUPnPServiceAsync::BeginSCPDDownload","upnp.iupnpserviceasync_beginscpddownload","upnp/IUPnPServiceAsync::BeginSCPDDownload"]
old-location: upnp\iupnpserviceasync_beginscpddownload.htm
tech.root: upnp
ms.assetid: CA573855-6D86-4C6C-B557-F8E8776BDBD3
ms.date: 12/05/2018
ms.keywords: BeginSCPDDownload, BeginSCPDDownload method [UPnP APIs], BeginSCPDDownload method [UPnP APIs],IUPnPServiceAsync interface, IUPnPServiceAsync interface [UPnP APIs],BeginSCPDDownload method, IUPnPServiceAsync.BeginSCPDDownload, IUPnPServiceAsync::BeginSCPDDownload, upnp.iupnpserviceasync_beginscpddownload, upnp/IUPnPServiceAsync::BeginSCPDDownload
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Upnp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPServiceAsync::BeginSCPDDownload
 - upnp/IUPnPServiceAsync::BeginSCPDDownload
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPServiceAsync.BeginSCPDDownload
---

# IUPnPServiceAsync::BeginSCPDDownload


## -description

The <b>BeginSCPDDownload</b> method initiates the asynchronous download of an Service Control Protocol Description (SCPD) document.

## -parameters

### -param pAsyncResult [in, optional]

Specifies a pointer to an <a href="/windows/desktop/api/upnp/nn-upnp-iupnpasyncresult">IUPnPAsyncResult</a> object. When the <b>BeginSCPDDownload</b> call is complete, 
	UPnP will use the <a href="/windows/desktop/api/upnp/nf-upnp-iupnpasyncresult-asyncoperationcomplete">IUPnPAsyncResult::AsyncOperationComplete</a> method to notify the control 
	point.

### -param pullRequestID [out]

Pointer to a 64-bit <b>ULONG</b> value used to identify the <b>BeginSCPDDownload</b> operation requested prior to this call.

## -returns

Returns <b>S_OK</b> on success. Otherwise, the method returns a COM error code defined in <b>WinError.h</b> or one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failed to initiate the SCPD download.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pAsyncResult</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/upnp/nf-upnp-iupnpasyncresult-asyncoperationcomplete">IUPnPAsyncResult::AsyncOperationComplete</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpserviceasync">IUPnPServiceAsync</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-begininvokeaction">IUPnPServiceAsync::BeginInvokeAction</a>
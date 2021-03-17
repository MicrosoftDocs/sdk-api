---
UID: NF:upnp.IUPnPServiceAsync.CancelAsyncOperation
title: IUPnPServiceAsync::CancelAsyncOperation (upnp.h)
description: CancelAsyncOperation method cancels a pending asynchronous operation initiated by the BeginInvokeAction, BeginQueryStateVariable, BeginSubscribeToEvents, or BeginSCPDDownload methods.
helpviewer_keywords: ["CancelAsyncOperation","CancelAsyncOperation method [UPnP APIs]","CancelAsyncOperation method [UPnP APIs]","IUPnPServiceAsync interface","IUPnPServiceAsync interface [UPnP APIs]","CancelAsyncOperation method","IUPnPServiceAsync.CancelAsyncOperation","IUPnPServiceAsync::CancelAsyncOperation","upnp.iupnpserviceasync_cancelasyncoperation","upnp/IUPnPServiceAsync::CancelAsyncOperation"]
old-location: upnp\iupnpserviceasync_cancelasyncoperation.htm
tech.root: upnp
ms.assetid: FBEC2DF3-6D45-49F2-AAA8-6DED697BC5A6
ms.date: 12/05/2018
ms.keywords: CancelAsyncOperation, CancelAsyncOperation method [UPnP APIs], CancelAsyncOperation method [UPnP APIs],IUPnPServiceAsync interface, IUPnPServiceAsync interface [UPnP APIs],CancelAsyncOperation method, IUPnPServiceAsync.CancelAsyncOperation, IUPnPServiceAsync::CancelAsyncOperation, upnp.iupnpserviceasync_cancelasyncoperation, upnp/IUPnPServiceAsync::CancelAsyncOperation
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
 - IUPnPServiceAsync::CancelAsyncOperation
 - upnp/IUPnPServiceAsync::CancelAsyncOperation
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
 - IUPnPServiceAsync.CancelAsyncOperation
---

# IUPnPServiceAsync::CancelAsyncOperation


## -description

The <b>CancelAsyncOperation</b> method cancels a pending asynchronous operation initiated by the <a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-begininvokeaction">BeginInvokeAction</a>, <a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginquerystatevariable">BeginQueryStateVariable</a>,  <a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginsubscribetoevents">BeginSubscribeToEvents</a>, or <a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginscpddownload">BeginSCPDDownload</a> methods.

## -parameters

### -param ullRequestID [in]

A 64-bit <b>ULONG</b> value that corresponds to the pending asynchronous UPnP operation.

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
Failed to cancel the asynchronous operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ullRequestID</i> does not match the pending asynchronous call.

</td>
</tr>
</table>

## -remarks

Calling this method for a pending <a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginscpddownload">BeginSCPDDownload</a> operation the SCPD download will still take place in the background, but will not notify callbacks of events associated with the operation.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpserviceasync">IUPnPServiceAsync</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-begininvokeaction">IUPnPServiceAsync::BeginInvokeAction</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginquerystatevariable">IUPnPServiceAsync::BeginQueryStateVariable</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginscpddownload">IUPnPServiceAsync::BeginSCPDDownload</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginsubscribetoevents">IUPnPServiceAsync::BeginSubscribeToEvents</a>
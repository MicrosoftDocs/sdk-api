---
UID: NF:upnp.IUPnPServiceAsync.EndSCPDDownload
title: IUPnPServiceAsync::EndSCPDDownload (upnp.h)
description: EndSCPDDownload method retrieves the results of a previous asynchronous download of an Service Control Protocol Description (SCPD) document.
helpviewer_keywords: ["EndSCPDDownload","EndSCPDDownload method [UPnP APIs]","EndSCPDDownload method [UPnP APIs]","IUPnPServiceAsync interface","IUPnPServiceAsync interface [UPnP APIs]","EndSCPDDownload method","IUPnPServiceAsync.EndSCPDDownload","IUPnPServiceAsync::EndSCPDDownload","upnp.iupnpserviceasync_endscpddownload","upnp/IUPnPServiceAsync::EndSCPDDownload"]
old-location: upnp\iupnpserviceasync_endscpddownload.htm
tech.root: upnp
ms.assetid: 1C4F7986-9282-4775-B9B2-338AC44F2243
ms.date: 12/05/2018
ms.keywords: EndSCPDDownload, EndSCPDDownload method [UPnP APIs], EndSCPDDownload method [UPnP APIs],IUPnPServiceAsync interface, IUPnPServiceAsync interface [UPnP APIs],EndSCPDDownload method, IUPnPServiceAsync.EndSCPDDownload, IUPnPServiceAsync::EndSCPDDownload, upnp.iupnpserviceasync_endscpddownload, upnp/IUPnPServiceAsync::EndSCPDDownload
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
 - IUPnPServiceAsync::EndSCPDDownload
 - upnp/IUPnPServiceAsync::EndSCPDDownload
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
 - IUPnPServiceAsync.EndSCPDDownload
---

# IUPnPServiceAsync::EndSCPDDownload


## -description

The <b>EndSCPDDownload</b> method retrieves the results of  a previous asynchronous download of an Service Control Protocol Description (SCPD) document.

## -parameters

### -param ullRequestID

Pointer to a 64-bit <b>ULONG</b> value that corresponds to the <a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginscpddownload">BeginSCPDDownload</a> operation requested prior to this call.

### -param pbstrSCPDDoc [out]

A  buffer containing the SCPD document.

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
Failed to finalize the SCPD download and retrieve the document string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ullRequestID</i> does not match the pending async call.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpserviceasync">IUPnPServiceAsync</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginscpddownload">IUPnPServiceAsync::BeginSCPDDownload</a>
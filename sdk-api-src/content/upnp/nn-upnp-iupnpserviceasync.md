---
UID: NN:upnp.IUPnPServiceAsync
title: IUPnPServiceAsync (upnp.h)

description: Use this interface to asynchronously query state variables and invoke actions on an instance of a service .
old-location: upnp\iupnpserviceasync.htm
tech.root: upnp
ms.assetid: B77025D6-26C7-46C9-84FE-69685C61735D

ms.date: 12/05/2018
ms.keywords: IUPnPServiceAsync, IUPnPServiceAsync interface [UPnP APIs], IUPnPServiceAsync interface [UPnP APIs],described, upnp.iupnpserviceasync, upnp/IUPnPServiceAsync
ms.topic: interface
f1_keywords: 
 - "upnp/IUPnPServiceAsync"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPServiceAsync
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPServiceAsync interface


## -description


Use this interface to asynchronously query state variables and invoke actions on an instance of a service .

This interface can be obtained through a <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> off the <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nn-upnp-iupnpservice">IUPnPService</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPServiceAsync</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPServiceAsync</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPServiceAsync</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-begininvokeaction">BeginInvokeAction</a>
</td>
<td align="left" width="63%">
Invokes an action on a device in asynchronous mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginquerystatevariable">BeginQueryStateVariable</a>
</td>
<td align="left" width="63%">
Initiates a request for the state variable value for a specific service in asynchronous mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginscpddownload">BeginSCPDDownload</a>
</td>
<td align="left" width="63%">
Initiates asynchronous download of the Service Control Protocol Description (SCPD) document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginsubscribetoevents">BeginSubscribeToEvents</a>
</td>
<td align="left" width="63%">
Initiates the registration of an application callback with the UPnP framework in asynchronous mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-cancelasyncoperation">CancelAsyncOperation</a>
</td>
<td align="left" width="63%">
Cancels any asynchronous operation initiated by the <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-begininvokeaction">BeginInvokeAction</a>, <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginquerystatevariable">BeginQueryStateVariable</a>, <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginsubscribetoevents">BeginSubscribeToEvents</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginscpddownload">BeginSCPDDownload</a> methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-endinvokeaction">EndInvokeAction</a>
</td>
<td align="left" width="63%">
Finalizes a <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-begininvokeaction">BeginInvokeAction</a> operation and retrieves the resultant output arguments.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-endquerystatevariable">EndQueryStateVariable</a>
</td>
<td align="left" width="63%">
Retrieves the service state variable value requested by <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginquerystatevariable">BeginQueryStateVariable</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-endscpddownload">EndSPCDDownload</a>
</td>
<td align="left" width="63%">
Finalizes asynchronous download of the Service Control Protocol Description (SCPD) document initiated by <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginscpddownload">BeginSCPDDownload</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-endsubscribetoevents">EndSubscribeToEvents</a>
</td>
<td align="left" width="63%">
Finalizes the <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceasync-beginsubscribetoevents">BeginSubscribeToEvents</a> operation. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nn-upnp-iupnpasyncresult">IUPnPAsyncResult</a>
 

 


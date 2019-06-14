---
UID: NN:wtsprotocol.IWTSProtocolConnectionCallback
title: IWTSProtocolConnectionCallback (wtsprotocol.h)
author: windows-sdk-content
description: IWTSProtocolConnectionCallback is no longer available. Instead, use IWRdsProtocolConnectionCallback.
old-location: termserv\iwtsprotocolconnectioncallback.htm
tech.root: TermServ
ms.assetid: ac8a2a66-fa1f-48bd-9502-def833e26f31
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWTSProtocolConnectionCallback, IWTSProtocolConnectionCallback interface [Remote Desktop Services], IWTSProtocolConnectionCallback interface [Remote Desktop Services],described, termserv.iwtsprotocolconnectioncallback, wtsprotocol/IWTSProtocolConnectionCallback
ms.topic: interface
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWTSProtocolConnectionCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSProtocolConnectionCallback interface


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnectionCallback</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback">IWRdsProtocolConnectionCallback</a>.]

 Exposes methods that provide information about the status of a client connection and that perform actions for the client. This interface is implemented by the Remote Desktop Services service and called by the protocol.

An instance of this interface is associated with a specific instance of the <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a> interface. When the following documentation refers to a connection, it is therefore referring to the specific connection for which the  <b>IWTSProtocolConnection</b> object was created.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSProtocolConnectionCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSProtocolConnectionCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSProtocolConnectionCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnectioncallback-brokenconnection">BrokenConnection</a>
</td>
<td align="left" width="63%">
Informs the Remote Desktop Services service that the client connection has been lost.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnectioncallback-displayioctl">DisplayIOCtl</a>
</td>
<td align="left" width="63%">
Requests that the Remote Desktop Services service send data to the display driver loaded in the session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnectioncallback-onready">OnReady</a>
</td>
<td align="left" width="63%">
Requests that the Remote Desktop Services service continue the connection process for that client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnectioncallback-redrawwindow">RedrawWindow</a>
</td>
<td align="left" width="63%">
Requests that the Remote Desktop Services service redraw the client window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnectioncallback-stopscreenupdates">StopScreenUpdates</a>
</td>
<td align="left" width="63%">
Requests that the Remote Desktop Services service stop updating the client screen.

</td>
</tr>
</table> 


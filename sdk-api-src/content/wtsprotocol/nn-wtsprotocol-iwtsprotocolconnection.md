---
UID: NN:wtsprotocol.IWTSProtocolConnection
title: IWTSProtocolConnection (wtsprotocol.h)
description: IWTSProtocolConnection is no longer available. Instead, use IWRdsProtocolConnection.
helpviewer_keywords: ["IWTSProtocolConnection","IWTSProtocolConnection interface [Remote Desktop Services]","IWTSProtocolConnection interface [Remote Desktop Services]","described","termserv.iwtsprotocolconnection","wtsprotocol/IWTSProtocolConnection"]
old-location: termserv\iwtsprotocolconnection.htm
tech.root: TermServ
ms.assetid: 584a6874-0df4-480e-a10a-4b603643870e
ms.date: 12/05/2018
ms.keywords: IWTSProtocolConnection, IWTSProtocolConnection interface [Remote Desktop Services], IWTSProtocolConnection interface [Remote Desktop Services],described, termserv.iwtsprotocolconnection, wtsprotocol/IWTSProtocolConnection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWTSProtocolConnection
 - wtsprotocol/IWTSProtocolConnection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWTSProtocolConnection
---

# IWTSProtocolConnection interface


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>.]

  Exposes methods called by the Remote Desktop Services service to configure a client connection. Your protocol must implement this interface to handle connection requests from clients. When the protocol listener receives a connection request from a client, it must create an <b>IWTSProtocolConnection</b> object and pass it to the Remote Desktop Services service by calling  the <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocollistenercallback-onconnected">OnConnected</a> method. In response, the service adds a reference to the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnectioncallback">IWTSProtocolConnectionCallback</a> object and returns a pointer to it. When the connection is no longer needed, the protocol must release the pointer.

During a connection sequence, the following methods are called by the Remote Desktop Services service in the order listed.
<ol>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlogonerrorredirector">GetLogonErrorRedirector</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendpolicydata">SendPolicyData</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-acceptconnection">AcceptConnection</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getclientdata">GetClientData</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getusercredentials">GetUserCredentials</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlicenseconnection">GetLicenseConnection</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-authenticateclienttosession">AuthenticateClientToSession</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-notifysessionid">NotifySessionId</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolhandles">GetProtocolHandles</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-connectnotify">ConnectNotify</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-isuserallowedtologon">IsUserAllowedToLogon</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sessionarbitrationenumeration">SessionArbitrationEnumeration</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-logonnotify">LogonNotify</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getuserdata">GetUserData</a>
</li>
</ol>If the Remote Desktop Services service needs to reconnect after calling <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sessionarbitrationenumeration">SessionArbitrationEnumeration</a>, it reconnects by calling the following methods in the order listed:
<ol>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-disconnectnotify">DisconnectNotify</a> (Called on the new session that was created.)</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-notifysessionid">NotifySessionId</a> (Called on the existing session.)</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolhandles">GetProtocolHandles</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-connectnotify">ConnectNotify</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-logonnotify">LogonNotify</a>
</li>
</ol>To disconnect, the Remote Desktop Services service calls the following methods in the order listed:
<ol>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-disconnectnotify">DisconnectNotify</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-close">Close</a>
</li>
</ol>The Remote Desktop Services service can call the following methods at any time after a connection has been established:
<ul>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolstatus">GetProtocolStatus</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlastinputtime">GetLastInputTime</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-seterrorinfo">SetErrorInfo</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendbeep">SendBeep</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-createvirtualchannel">CreateVirtualChannel</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty">QueryProperty</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getshadowconnection">GetShadowConnection</a>
</li>
</ul>

## -inheritance

The <b>IWTSProtocolConnection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSProtocolConnection</b> also has these types of members:


---
UID: NN:wtsprotocol.IWRdsProtocolConnection
title: IWRdsProtocolConnection (wtsprotocol.h)
description: Exposes methods called by the Remote Desktop Services service to configure a client connection.
helpviewer_keywords: ["IWRdsProtocolConnection","IWRdsProtocolConnection interface [Remote Desktop Services]","IWRdsProtocolConnection interface [Remote Desktop Services]","described","termserv.iwrdsprotocolconnection","wtsprotocol/IWRdsProtocolConnection"]
old-location: termserv\iwrdsprotocolconnection.htm
tech.root: TermServ
ms.assetid: 2b8a5b2f-5a54-4d60-8b5a-8a914728087c
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolConnection, IWRdsProtocolConnection interface [Remote Desktop Services], IWRdsProtocolConnection interface [Remote Desktop Services],described, termserv.iwrdsprotocolconnection, wtsprotocol/IWRdsProtocolConnection
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - IWRdsProtocolConnection
 - wtsprotocol/IWRdsProtocolConnection
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
 - IWRdsProtocolConnection
---

# IWRdsProtocolConnection interface


## -description

Exposes methods called by the Remote Desktop Services service to configure a client connection. Your protocol must implement this interface to handle connection requests from clients. When the protocol listener receives a connection request from a client, it must create an <b>IWRdsProtocolConnection</b> object and pass it to the Remote Desktop Services service by calling  the <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected">IWRdsProtocolListenerCallback::OnConnected</a> method. In response, the service adds a reference to the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback">IWRdsProtocolConnectionCallback</a> object and returns a pointer to it. When the connection is no longer needed, the protocol must release the pointer.

During a connection sequence, the following methods are called by the Remote Desktop Services service in the order listed.
<ol>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getlogonerrorredirector">GetLogonErrorRedirector</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-acceptconnection">AcceptConnection</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getclientdata">GetClientData</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getclientmonitordata">GetClientMonitorData</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getusercredentials">GetUserCredentials</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getlicenseconnection">GetLicenseConnection</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-authenticateclienttosession">AuthenticateClientToSession</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-notifysessionid">NotifySessionId</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getinputhandles">GetInputHandles</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getvideohandle">GetVideoHandle</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-connectnotify">ConnectNotify</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-notifycommandprocesscreated">NotifyCommandProcessCreated</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-isuserallowedtologon">IsUserAllowedToLogon</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-sessionarbitrationenumeration">SessionArbitrationEnumeration</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-logonnotify">LogonNotify</a>
</li>
</ol>If the Remote Desktop Services service needs to reconnect after calling <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-sessionarbitrationenumeration">SessionArbitrationEnumeration</a>, it reconnects by calling the following methods in the order listed:
<ol>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-disconnectnotify">DisconnectNotify</a> (Called on the new session that was created.)</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-notifysessionid">NotifySessionId</a> (Called on the existing session.)</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getinputhandles">GetInputHandles</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getvideohandle">GetVideoHandle</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-connectnotify">ConnectNotify</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-logonnotify">LogonNotify</a>
</li>
</ol>To disconnect, the Remote Desktop Services service calls the following methods in the order listed:
<ol>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-predisconnect">PreDisconnect</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-disconnectnotify">DisconnectNotify</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-close">Close</a>
</li>
</ol>The Remote Desktop Services service can call the following methods at any time after a connection has been established:
<ul>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getprotocolstatus">GetProtocolStatus</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getlastinputtime">GetLastInputTime</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-seterrorinfo">SetErrorInfo</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-createvirtualchannel">CreateVirtualChannel</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty">QueryProperty</a>
</li>
<li>
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getshadowconnection">GetShadowConnection</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsProtocolConnection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWRdsProtocolConnection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWRdsProtocolConnection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-acceptconnection">AcceptConnection</a>
</td>
<td align="left" width="63%">
Directs the protocol to continue with the connection request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-authenticateclienttosession">AuthenticateClientToSession</a>
</td>
<td align="left" width="63%">
Specifies a session that the connection should be reconnected to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-close">Close</a>
</td>
<td align="left" width="63%">
Closes a connection after the session is disconnected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-connectnotify">ConnectNotify</a>
</td>
<td align="left" width="63%">
Signals the protocol that the session has been initialized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-createvirtualchannel">CreateVirtualChannel</a>
</td>
<td align="left" width="63%">
Requests that the protocol create a virtual channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-disconnectnotify">DisconnectNotify</a>
</td>
<td align="left" width="63%">
Notifies the protocol that the session has been disconnected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getclientdata">GetClientData</a>
</td>
<td align="left" width="63%">
Requests client settings from the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getclientmonitordata">GetClientMonitorData</a>
</td>
<td align="left" width="63%">
Retrieves the number of monitors and the primary monitor number on the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getinputhandles">GetInputHandles</a>
</td>
<td align="left" width="63%">
Obtains the handles to input/output devices for the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getlastinputtime">GetLastInputTime</a>
</td>
<td align="left" width="63%">
Retrieves the last time the protocol received user input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getlicenseconnection">GetLicenseConnection</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection">IWRdsProtocolLicenseConnection</a> object that is used to begin the client licensing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getlogonerrorredirector">GetLogonErrorRedirector</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector">IWRdsProtocolLogonErrorRedirector</a> interface that specifies how the protocol should handle client logon errors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getprotocolstatus">GetProtocolStatus</a>
</td>
<td align="left" width="63%">
Retrieves information about the protocol status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getshadowconnection">GetShadowConnection</a>
</td>
<td align="left" width="63%">
Retrieves a reference to the shadow connection object from the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getusercredentials">GetUserCredentials</a>
</td>
<td align="left" width="63%">
Returns user credentials.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-getvideohandle">GetVideoHandle</a>
</td>
<td align="left" width="63%">
Obtains the handle of the video device for the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-isuserallowedtologon">IsUserAllowedToLogon</a>
</td>
<td align="left" width="63%">
Determines from the protocol whether a user is allowed to log on to a session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-logonnotify">LogonNotify</a>
</td>
<td align="left" width="63%">
Called when the user has logged on to the session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-notifycommandprocesscreated">NotifyCommandProcessCreated</a>
</td>
<td align="left" width="63%">
Notifies the protocol that the Winlogon.exe process has been created and initialized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-notifysessionid">NotifySessionId</a>
</td>
<td align="left" width="63%">
Sends the identifier of the new session to the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-predisconnect">PreDisconnect</a>
</td>
<td align="left" width="63%">
Notifies the protocol that the session is about to be disconnected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty">QueryProperty</a>
</td>
<td align="left" width="63%">
Retrieves a property value from the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-sessionarbitrationenumeration">SessionArbitrationEnumeration</a>
</td>
<td align="left" width="63%">
Called after arbitration to allow the protocol to specify the sessions to be reconnected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-seterrorinfo">SetErrorInfo</a>
</td>
<td align="left" width="63%">
Sets error information in the protocol.

</td>
</tr>
</table>

## -remarks

To avoid a possible deadlock when calling any of the methods on this interface, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.
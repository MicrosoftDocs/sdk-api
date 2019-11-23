---
UID: NN:wtsprotocol.IWTSProtocolConnection
title: IWTSProtocolConnection (wtsprotocol.h)

description: IWTSProtocolConnection is no longer available. Instead, use IWRdsProtocolConnection.
old-location: termserv\iwtsprotocolconnection.htm
tech.root: TermServ
ms.assetid: 584a6874-0df4-480e-a10a-4b603643870e

ms.date: 12/05/2018
ms.keywords: IWTSProtocolConnection, IWTSProtocolConnection interface [Remote Desktop Services], IWTSProtocolConnection interface [Remote Desktop Services],described, termserv.iwtsprotocolconnection, wtsprotocol/IWTSProtocolConnection
ms.topic: interface
f1_keywords: 
 - "wtsprotocol/IWTSProtocolConnection"
dev_langs:
 - c++
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
 - IWTSProtocolConnection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSProtocolConnection interface


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>.]

  Exposes methods called by the Remote Desktop Services service to configure a client connection. Your protocol must implement this interface to handle connection requests from clients. When the protocol listener receives a connection request from a client, it must create an <b>IWTSProtocolConnection</b> object and pass it to the Remote Desktop Services service by calling  the <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocollistenercallback-onconnected">OnConnected</a> method. In response, the service adds a reference to the <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnectioncallback">IWTSProtocolConnectionCallback</a> object and returns a pointer to it. When the connection is no longer needed, the protocol must release the pointer.

During a connection sequence, the following methods are called by the Remote Desktop Services service in the order listed.
<ol>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlogonerrorredirector">GetLogonErrorRedirector</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendpolicydata">SendPolicyData</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-acceptconnection">AcceptConnection</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getclientdata">GetClientData</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getusercredentials">GetUserCredentials</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlicenseconnection">GetLicenseConnection</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-authenticateclienttosession">AuthenticateClientToSession</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-notifysessionid">NotifySessionId</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolhandles">GetProtocolHandles</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-connectnotify">ConnectNotify</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-isuserallowedtologon">IsUserAllowedToLogon</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sessionarbitrationenumeration">SessionArbitrationEnumeration</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-logonnotify">LogonNotify</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getuserdata">GetUserData</a>
</li>
</ol>If the Remote Desktop Services service needs to reconnect after calling <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sessionarbitrationenumeration">SessionArbitrationEnumeration</a>, it reconnects by calling the following methods in the order listed:
<ol>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-disconnectnotify">DisconnectNotify</a> (Called on the new session that was created.)</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-notifysessionid">NotifySessionId</a> (Called on the existing session.)</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolhandles">GetProtocolHandles</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-connectnotify">ConnectNotify</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-logonnotify">LogonNotify</a>
</li>
</ol>To disconnect, the Remote Desktop Services service calls the following methods in the order listed:
<ol>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-disconnectnotify">DisconnectNotify</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-close">Close</a>
</li>
</ol>The Remote Desktop Services service can call the following methods at any time after a connection has been established:
<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolstatus">GetProtocolStatus</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlastinputtime">GetLastInputTime</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-seterrorinfo">SetErrorInfo</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendbeep">SendBeep</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-createvirtualchannel">CreateVirtualChannel</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty">QueryProperty</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getshadowconnection">GetShadowConnection</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSProtocolConnection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSProtocolConnection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSProtocolConnection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-acceptconnection">AcceptConnection</a>
</td>
<td align="left" width="63%">
Directs the protocol to continue with the connection request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-authenticateclienttosession">AuthenticateClientToSession</a>
</td>
<td align="left" width="63%">
Specifies a session that the connection should be reconnected to. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-close">Close</a>
</td>
<td align="left" width="63%">
Closes a connection after the session is disconnected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-connectnotify">ConnectNotify</a>
</td>
<td align="left" width="63%">
Signals that the session has been initialized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-createvirtualchannel">CreateVirtualChannel</a>
</td>
<td align="left" width="63%">
Creates a static or dynamic virtual channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-disconnectnotify">DisconnectNotify</a>
</td>
<td align="left" width="63%">
Notifies the protocol that the session has been disconnected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getclientdata">GetClientData</a>
</td>
<td align="left" width="63%">
Requests client settings from the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlastinputtime">GetLastInputTime</a>
</td>
<td align="left" width="63%">
Returns the last time the protocol received input data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlicenseconnection">GetLicenseConnection</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollicenseconnection">IWTSProtocolLicenseConnection</a> object that is used to begin the client licensing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlogonerrorredirector">GetLogonErrorRedirector</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollogonerrorredirector">IWTSProtocolLogonErrorRedirector</a> interface that specifies how the protocol should handle client logon errors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolhandles">GetProtocolHandles</a>
</td>
<td align="left" width="63%">
Retrieves keyboard, mouse, sound, and beep handles supported by the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolstatus">GetProtocolStatus</a>
</td>
<td align="left" width="63%">
Retrieves information about the protocol status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getshadowconnection">GetShadowConnection</a>
</td>
<td align="left" width="63%">
Retrieves a  <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowconnection">IWTSProtocolShadowConnection</a> object from the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getusercredentials">GetUserCredentials</a>
</td>
<td align="left" width="63%">
Returns user credentials.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getuserdata">GetUserData</a>
</td>
<td align="left" width="63%">
Sends merged policy settings to the protocol and requests user policy settings from the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-isuserallowedtologon">IsUserAllowedToLogon</a>
</td>
<td align="left" width="63%">
Determines whether a user is allowed to log on to a session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-logonnotify">LogonNotify</a>
</td>
<td align="left" width="63%">
Specifies that the user has logged on to the session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-notifysessionid">NotifySessionId</a>
</td>
<td align="left" width="63%">
Sends the ID of  the new session to the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty">QueryProperty</a>
</td>
<td align="left" width="63%">
Retrieves the specified property from the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendbeep">SendBeep</a>
</td>
<td align="left" width="63%">
Sends a sound pulse to the console speaker on the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendpolicydata">SendPolicyData</a>
</td>
<td align="left" width="63%">
Sends computer policy settings to the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sessionarbitrationenumeration">SessionArbitrationEnumeration</a>
</td>
<td align="left" width="63%">
Retrieves a collection of session IDs for reconnection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-seterrorinfo">SetErrorInfo</a>
</td>
<td align="left" width="63%">
Sends an error code to the client.

</td>
</tr>
</table> 


---
UID: NN:wtsprotocol.IWRdsProtocolConnection
title: IWRdsProtocolConnection
author: windows-sdk-content
description: Exposes methods called by the Remote Desktop Services service to configure a client connection.
old-location: termserv\iwrdsprotocolconnection.htm
tech.root: termserv
ms.assetid: 2b8a5b2f-5a54-4d60-8b5a-8a914728087c
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IWRdsProtocolConnection, IWRdsProtocolConnection interface [Remote Desktop Services], IWRdsProtocolConnection interface [Remote Desktop Services],described, termserv.iwrdsprotocolconnection, wtsprotocol/IWRdsProtocolConnection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolConnection interface


## -description


Exposes methods called by the Remote Desktop Services service to configure a client connection. Your protocol must implement this interface to handle connection requests from clients. When the protocol listener receives a connection request from a client, it must create an <b>IWRdsProtocolConnection</b> object and pass it to the Remote Desktop Services service by calling  the <a href="https://msdn.microsoft.com/9d2d5393-f0a6-40ec-9bf2-2e8c945693db">IWRdsProtocolListenerCallback::OnConnected</a> method. In response, the service adds a reference to the <a href="https://msdn.microsoft.com/81a73688-f39e-4960-8587-602d56c11e7e">IWRdsProtocolConnectionCallback</a> object and returns a pointer to it. When the connection is no longer needed, the protocol must release the pointer.

During a connection sequence, the following methods are called by the Remote Desktop Services service in the order listed.
<ol>
<li>
<a href="https://msdn.microsoft.com/9613330F-B8DE-48C7-892C-FB8F50739C13">GetLogonErrorRedirector</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ef7e13ad-eeb8-4452-b3d6-a137b766f98f">AcceptConnection</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4005ff92-56ea-46ae-a546-e08a80303ef5">GetClientData</a>
</li>
<li>
<a href="https://msdn.microsoft.com/df70ff56-3e12-4842-a818-31ee75da96a9">GetClientMonitorData</a>
</li>
<li>
<a href="https://msdn.microsoft.com/dcd8de76-e260-4b3b-98ca-4f486b3b6635">GetUserCredentials</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6c75f80a-0d47-489d-b684-f718326e2b0d">GetLicenseConnection</a>
</li>
<li>
<a href="https://msdn.microsoft.com/314f1ae8-5b2d-4c95-bb2d-0d9288d38934">AuthenticateClientToSession</a>
</li>
<li>
<a href="https://msdn.microsoft.com/82bf892e-5e6f-4057-ac36-00e046080c93">NotifySessionId</a>
</li>
<li>
<a href="https://msdn.microsoft.com/42f20dfc-e625-4b53-b055-750af4cbd3ec">GetInputHandles</a>
</li>
<li>
<a href="https://msdn.microsoft.com/069ee899-ae3a-4043-92b5-e193dbfe4f54">GetVideoHandle</a>
</li>
<li>
<a href="https://msdn.microsoft.com/057a093b-9b2d-4a2e-9593-fe0251427be0">ConnectNotify</a>
</li>
<li>
<a href="https://msdn.microsoft.com/B2A9CC5A-6E6E-418D-9C03-FDF207AFB683">NotifyCommandProcessCreated</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4e2c5d2b-ec45-45ea-8bd3-71aaa0b15529">IsUserAllowedToLogon</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d0e93014-1f79-47ac-bf3a-c100eb652751">SessionArbitrationEnumeration</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2b6ce1cd-0e9f-465d-a5d6-e0d35bddebc4">LogonNotify</a>
</li>
</ol>If the Remote Desktop Services service needs to reconnect after calling <a href="https://msdn.microsoft.com/d0e93014-1f79-47ac-bf3a-c100eb652751">SessionArbitrationEnumeration</a>, it reconnects by calling the following methods in the order listed:
<ol>
<li>
<a href="https://msdn.microsoft.com/2399677b-0859-4e43-9dbc-0b08fa0647b0">DisconnectNotify</a> (Called on the new session that was created.)</li>
<li>
<a href="https://msdn.microsoft.com/82bf892e-5e6f-4057-ac36-00e046080c93">NotifySessionId</a> (Called on the existing session.)</li>
<li>
<a href="https://msdn.microsoft.com/42f20dfc-e625-4b53-b055-750af4cbd3ec">GetInputHandles</a>
</li>
<li>
<a href="https://msdn.microsoft.com/069ee899-ae3a-4043-92b5-e193dbfe4f54">GetVideoHandle</a>
</li>
<li>
<a href="https://msdn.microsoft.com/057a093b-9b2d-4a2e-9593-fe0251427be0">ConnectNotify</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2b6ce1cd-0e9f-465d-a5d6-e0d35bddebc4">LogonNotify</a>
</li>
</ol>To disconnect, the Remote Desktop Services service calls the following methods in the order listed:
<ol>
<li>
<a href="https://msdn.microsoft.com/988032B5-94AA-40ED-B571-E7C2E652D023">PreDisconnect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2399677b-0859-4e43-9dbc-0b08fa0647b0">DisconnectNotify</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8d159e3f-b429-4522-b608-0068b1f7fa4e">Close</a>
</li>
</ol>The Remote Desktop Services service can call the following methods at any time after a connection has been established:
<ul>
<li>
<a href="https://msdn.microsoft.com/A89C2E3F-AC75-4CFB-9DA7-00DCEDCA1C1A">GetProtocolStatus</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1a6acbd2-6155-4513-8892-50a4552abb12">GetLastInputTime</a>
</li>
<li>
<a href="https://msdn.microsoft.com/114abaf1-fe67-4d80-ad5d-f49aac9dd587">SetErrorInfo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c0302081-06af-44af-a9ed-936d705e711b">CreateVirtualChannel</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d504a40f-5dc5-4c1b-960f-d41cccef9154">QueryProperty</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1b1059af-f673-47fd-85fc-57df76adfbcf">GetShadowConnection</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsProtocolConnection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWRdsProtocolConnection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ef7e13ad-eeb8-4452-b3d6-a137b766f98f">AcceptConnection</a>
</td>
<td align="left" width="63%">
Directs the protocol to continue with the connection request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/314f1ae8-5b2d-4c95-bb2d-0d9288d38934">AuthenticateClientToSession</a>
</td>
<td align="left" width="63%">
Specifies a session that the connection should be reconnected to.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d159e3f-b429-4522-b608-0068b1f7fa4e">Close</a>
</td>
<td align="left" width="63%">
Closes a connection after the session is disconnected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/057a093b-9b2d-4a2e-9593-fe0251427be0">ConnectNotify</a>
</td>
<td align="left" width="63%">
Signals the protocol that the session has been initialized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0302081-06af-44af-a9ed-936d705e711b">CreateVirtualChannel</a>
</td>
<td align="left" width="63%">
Requests that the protocol create a virtual channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2399677b-0859-4e43-9dbc-0b08fa0647b0">DisconnectNotify</a>
</td>
<td align="left" width="63%">
Notifies the protocol that the session has been disconnected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4005ff92-56ea-46ae-a546-e08a80303ef5">GetClientData</a>
</td>
<td align="left" width="63%">
Requests client settings from the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df70ff56-3e12-4842-a818-31ee75da96a9">GetClientMonitorData</a>
</td>
<td align="left" width="63%">
Retrieves the number of monitors and the primary monitor number on the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42f20dfc-e625-4b53-b055-750af4cbd3ec">GetInputHandles</a>
</td>
<td align="left" width="63%">
Obtains the handles to input/output devices for the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a6acbd2-6155-4513-8892-50a4552abb12">GetLastInputTime</a>
</td>
<td align="left" width="63%">
Retrieves the last time the protocol received user input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c75f80a-0d47-489d-b684-f718326e2b0d">GetLicenseConnection</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/498c31c5-1cb6-41d7-91fb-7409ea03dda0">IWRdsProtocolLicenseConnection</a> object that is used to begin the client licensing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9613330F-B8DE-48C7-892C-FB8F50739C13">GetLogonErrorRedirector</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/43c283f5-c902-49cc-81a0-15fc6316c7d4">IWRdsProtocolLogonErrorRedirector</a> interface that specifies how the protocol should handle client logon errors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A89C2E3F-AC75-4CFB-9DA7-00DCEDCA1C1A">GetProtocolStatus</a>
</td>
<td align="left" width="63%">
Retrieves information about the protocol status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b1059af-f673-47fd-85fc-57df76adfbcf">GetShadowConnection</a>
</td>
<td align="left" width="63%">
Retrieves a reference to the shadow connection object from the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dcd8de76-e260-4b3b-98ca-4f486b3b6635">GetUserCredentials</a>
</td>
<td align="left" width="63%">
Returns user credentials.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/069ee899-ae3a-4043-92b5-e193dbfe4f54">GetVideoHandle</a>
</td>
<td align="left" width="63%">
Obtains the handle of the video device for the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e2c5d2b-ec45-45ea-8bd3-71aaa0b15529">IsUserAllowedToLogon</a>
</td>
<td align="left" width="63%">
Determines from the protocol whether a user is allowed to log on to a session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b6ce1cd-0e9f-465d-a5d6-e0d35bddebc4">LogonNotify</a>
</td>
<td align="left" width="63%">
Called when the user has logged on to the session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B2A9CC5A-6E6E-418D-9C03-FDF207AFB683">NotifyCommandProcessCreated</a>
</td>
<td align="left" width="63%">
Notifies the protocol that the Winlogon.exe process has been created and initialized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82bf892e-5e6f-4057-ac36-00e046080c93">NotifySessionId</a>
</td>
<td align="left" width="63%">
Sends the identifier of the new session to the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/988032B5-94AA-40ED-B571-E7C2E652D023">PreDisconnect</a>
</td>
<td align="left" width="63%">
Notifies the protocol that the session is about to be disconnected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d504a40f-5dc5-4c1b-960f-d41cccef9154">QueryProperty</a>
</td>
<td align="left" width="63%">
Retrieves a property value from the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0e93014-1f79-47ac-bf3a-c100eb652751">SessionArbitrationEnumeration</a>
</td>
<td align="left" width="63%">
Called after arbitration to allow the protocol to specify the sessions to be reconnected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/114abaf1-fe67-4d80-ad5d-f49aac9dd587">SetErrorInfo</a>
</td>
<td align="left" width="63%">
Sets error information in the protocol.

</td>
</tr>
</table> 


## -remarks



To avoid a possible deadlock when calling any of the methods on this interface, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.




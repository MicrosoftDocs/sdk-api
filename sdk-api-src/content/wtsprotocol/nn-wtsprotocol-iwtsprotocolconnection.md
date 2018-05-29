---
UID: NN:wtsprotocol.IWTSProtocolConnection
title: IWTSProtocolConnection
author: windows-sdk-content
description: IWTSProtocolConnection is no longer available. Instead, use IWRdsProtocolConnection.
old-location: termserv\iwtsprotocolconnection.htm
old-project: TermServ
ms.assetid: 584a6874-0df4-480e-a10a-4b603643870e
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IWTSProtocolConnection, IWTSProtocolConnection interface [Remote Desktop Services], IWTSProtocolConnection interface [Remote Desktop Services],described, termserv.iwtsprotocolconnection, wtsprotocol/IWTSProtocolConnection
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wtsprotocol.h
api_name:
-	IWTSProtocolConnection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolConnection interface


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a>.]

  Exposes methods called by the Remote Desktop Services service to configure a client connection. Your protocol must implement this interface to handle connection requests from clients. When the protocol listener receives a connection request from a client, it must create an <b>IWTSProtocolConnection</b> object and pass it to the Remote Desktop Services service by calling  the <a href="https://msdn.microsoft.com/0874c394-6260-4ac1-b5a8-27879f562e19">OnConnected</a> method. In response, the service adds a reference to the <a href="https://msdn.microsoft.com/ac8a2a66-fa1f-48bd-9502-def833e26f31">IWTSProtocolConnectionCallback</a> object and returns a pointer to it. When the connection is no longer needed, the protocol must release the pointer.

During a connection sequence, the following methods are called by the Remote Desktop Services service in the order listed.
<ol>
<li>
<a href="https://msdn.microsoft.com/59bd7d50-2903-42b7-b556-4da7b50d8e7a">GetLogonErrorRedirector</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b3fcc213-8257-433f-b304-ce19bc209591">SendPolicyData</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5be00911-f68a-410d-8d56-81458b5ff44e">AcceptConnection</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1330fbb4-4c10-493b-ad95-3c2ad975459a">GetClientData</a>
</li>
<li>
<a href="https://msdn.microsoft.com/48cd1a57-5f6d-4feb-889d-7441a76c0410">GetUserCredentials</a>
</li>
<li>
<a href="https://msdn.microsoft.com/714e2479-54b2-4899-9fbd-68fa35051f58">GetLicenseConnection</a>
</li>
<li>
<a href="https://msdn.microsoft.com/541bf463-9a4a-4237-8a61-1288ab1540cc">AuthenticateClientToSession</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5a545f66-7143-419d-9e0c-a96070472ce5">NotifySessionId</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d453ac71-4733-4a68-892c-ffca2d2954c6">GetProtocolHandles</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9109d867-d9dc-4b95-a674-9f59ed7aa6a4">ConnectNotify</a>
</li>
<li>
<a href="https://msdn.microsoft.com/297ecc6c-6598-4c1a-94df-9d9924917cdf">IsUserAllowedToLogon</a>
</li>
<li>
<a href="https://msdn.microsoft.com/413d6df5-419f-4a68-bb91-dfec9f455b42">SessionArbitrationEnumeration</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6065e827-23a5-4150-bda5-999b7acede65">LogonNotify</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fa77c537-c78d-4fe3-b597-787efd740cf6">GetUserData</a>
</li>
</ol>If the Remote Desktop Services service needs to reconnect after calling <a href="https://msdn.microsoft.com/413d6df5-419f-4a68-bb91-dfec9f455b42">SessionArbitrationEnumeration</a>, it reconnects by calling the following methods in the order listed:
<ol>
<li>
<a href="https://msdn.microsoft.com/d2712d53-2e52-49d9-874e-e6425235d3f0">DisconnectNotify</a> (Called on the new session that was created.)</li>
<li>
<a href="https://msdn.microsoft.com/5a545f66-7143-419d-9e0c-a96070472ce5">NotifySessionId</a> (Called on the existing session.)</li>
<li>
<a href="https://msdn.microsoft.com/d453ac71-4733-4a68-892c-ffca2d2954c6">GetProtocolHandles</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9109d867-d9dc-4b95-a674-9f59ed7aa6a4">ConnectNotify</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6065e827-23a5-4150-bda5-999b7acede65">LogonNotify</a>
</li>
</ol>To disconnect, the Remote Desktop Services service calls the following methods in the order listed:
<ol>
<li>
<a href="https://msdn.microsoft.com/d2712d53-2e52-49d9-874e-e6425235d3f0">DisconnectNotify</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</li>
</ol>The Remote Desktop Services service can call the following methods at any time after a connection has been established:
<ul>
<li>
<a href="https://msdn.microsoft.com/d224877a-649a-4ac2-a5e7-831592e6a0d9">GetProtocolStatus</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8daecbde-8866-4ae9-a07c-32d28d321392">GetLastInputTime</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0ec35560-5aad-403a-9477-50e48ee7136a">SetErrorInfo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4665917d-4bc3-4017-9b69-3eb95e70337f">SendBeep</a>
</li>
<li>
<a href="https://msdn.microsoft.com/28cdabde-980f-48b7-920e-1eeeb70b6952">CreateVirtualChannel</a>
</li>
<li>
<a href="https://msdn.microsoft.com/129b8314-fa84-414d-93c4-f9320650e2de">QueryProperty</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6496deba-6166-48d2-9294-286a448de231">GetShadowConnection</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSProtocolConnection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWTSProtocolConnection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5be00911-f68a-410d-8d56-81458b5ff44e">AcceptConnection</a>
</td>
<td align="left" width="63%">
Directs the protocol to continue with the connection request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/541bf463-9a4a-4237-8a61-1288ab1540cc">AuthenticateClientToSession</a>
</td>
<td align="left" width="63%">
Specifies a session that the connection should be reconnected to. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Closes a connection after the session is disconnected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9109d867-d9dc-4b95-a674-9f59ed7aa6a4">ConnectNotify</a>
</td>
<td align="left" width="63%">
Signals that the session has been initialized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28cdabde-980f-48b7-920e-1eeeb70b6952">CreateVirtualChannel</a>
</td>
<td align="left" width="63%">
Creates a static or dynamic virtual channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2712d53-2e52-49d9-874e-e6425235d3f0">DisconnectNotify</a>
</td>
<td align="left" width="63%">
Notifies the protocol that the session has been disconnected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1330fbb4-4c10-493b-ad95-3c2ad975459a">GetClientData</a>
</td>
<td align="left" width="63%">
Requests client settings from the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8daecbde-8866-4ae9-a07c-32d28d321392">GetLastInputTime</a>
</td>
<td align="left" width="63%">
Returns the last time the protocol received input data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/714e2479-54b2-4899-9fbd-68fa35051f58">GetLicenseConnection</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/3f6925b6-c712-40c6-8b48-7df8ef4a9872">IWTSProtocolLicenseConnection</a> object that is used to begin the client licensing process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59bd7d50-2903-42b7-b556-4da7b50d8e7a">GetLogonErrorRedirector</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/1ff30217-9091-47df-a38f-30784538f0b9">IWTSProtocolLogonErrorRedirector</a> interface that specifies how the protocol should handle client logon errors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d453ac71-4733-4a68-892c-ffca2d2954c6">GetProtocolHandles</a>
</td>
<td align="left" width="63%">
Retrieves keyboard, mouse, sound, and beep handles supported by the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d224877a-649a-4ac2-a5e7-831592e6a0d9">GetProtocolStatus</a>
</td>
<td align="left" width="63%">
Retrieves information about the protocol status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6496deba-6166-48d2-9294-286a448de231">GetShadowConnection</a>
</td>
<td align="left" width="63%">
Retrieves a  <a href="https://msdn.microsoft.com/83285a6a-903f-4c23-8f62-b04bbeaa52f9">IWTSProtocolShadowConnection</a> object from the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48cd1a57-5f6d-4feb-889d-7441a76c0410">GetUserCredentials</a>
</td>
<td align="left" width="63%">
Returns user credentials.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa77c537-c78d-4fe3-b597-787efd740cf6">GetUserData</a>
</td>
<td align="left" width="63%">
Sends merged policy settings to the protocol and requests user policy settings from the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/297ecc6c-6598-4c1a-94df-9d9924917cdf">IsUserAllowedToLogon</a>
</td>
<td align="left" width="63%">
Determines whether a user is allowed to log on to a session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6065e827-23a5-4150-bda5-999b7acede65">LogonNotify</a>
</td>
<td align="left" width="63%">
Specifies that the user has logged on to the session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a545f66-7143-419d-9e0c-a96070472ce5">NotifySessionId</a>
</td>
<td align="left" width="63%">
Sends the ID of  the new session to the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/129b8314-fa84-414d-93c4-f9320650e2de">QueryProperty</a>
</td>
<td align="left" width="63%">
Retrieves the specified property from the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4665917d-4bc3-4017-9b69-3eb95e70337f">SendBeep</a>
</td>
<td align="left" width="63%">
Sends a sound pulse to the console speaker on the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3fcc213-8257-433f-b304-ce19bc209591">SendPolicyData</a>
</td>
<td align="left" width="63%">
Sends computer policy settings to the protocol.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/413d6df5-419f-4a68-bb91-dfec9f455b42">SessionArbitrationEnumeration</a>
</td>
<td align="left" width="63%">
Retrieves a collection of session IDs for reconnection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ec35560-5aad-403a-9477-50e48ee7136a">SetErrorInfo</a>
</td>
<td align="left" width="63%">
Sends an error code to the client.

</td>
</tr>
</table> 


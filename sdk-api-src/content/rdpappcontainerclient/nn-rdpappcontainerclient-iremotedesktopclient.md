---
UID: NN:rdpappcontainerclient.IRemoteDesktopClient
title: IRemoteDesktopClient
author: windows-driver-content
description: Provides methods and properties used to configure and use the Remote Desktop Protocol (RDP) app container client control.
old-location: termserv\iremotedesktopclient.htm
old-project: TermServ
ms.assetid: 4b4c1080-3ea1-4557-92d6-45a80a788071
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IRemoteDesktopClient, IRemoteDesktopClient interface [Remote Desktop Services], IRemoteDesktopClient interface [Remote Desktop Services],described, rdpappcontainerclient/IRemoteDesktopClient, termserv.iremotedesktopclient
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: rdpappcontainerclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsTscAx.dll
req.typenames: SnapshotFormatType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsTscAx.dll
api_name:
-	IRemoteDesktopClient
product: Windows
targetos: Windows
req.lib: 
req.dll: MsTscAx.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRemoteDesktopClient interface


## -description



Provides methods and properties used to configure and use the Remote Desktop Protocol (RDP) app container client control.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRemoteDesktopClient</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IRemoteDesktopClient</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRemoteDesktopClient</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a904827b-644b-459b-b1bd-399bad21f94f">attachEvent</a>
</td>
<td align="left" width="63%">
Attaches an event handler to an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52dbc0f3-8ba9-45a5-a224-b7de67847bf3">Connect</a>
</td>
<td align="left" width="63%">
Initiates a connection by using the properties currently set on the Remote Desktop Protocol (RDP) app container client control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9addc8de-1e82-47a3-a10e-566bacc3e37c">DeleteSavedCredentials</a>
</td>
<td align="left" width="63%">
Deletes saved credentials for the specified remote computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5913da44-3dc2-40a3-9808-3619e5fa91b4">detachEvent</a>
</td>
<td align="left" width="63%">
Detaches an event handler from an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/134e72ad-93dd-4f53-b26c-09654f309658">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects the active connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef000769-a2d8-4d62-99d9-33ffc18ec8f6">Reconnect</a>
</td>
<td align="left" width="63%">
Initiates an automatic reconnection of the Remote Desktop Protocol (RDP) app container client control to fit the session to the new width and height.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8a7f2b7-925a-49b8-aa7b-c59736a13c67">UpdateSessionDisplaySettings</a>
</td>
<td align="left" width="63%">
Updates the width and height settings for the Remote Desktop Protocol (RDP) app container client control.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRemoteDesktopClient</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/54ff5568-046e-42de-9b7c-b8c8c9be815c">Actions</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the actions object for the Remote Desktop Protocol (RDP) app container client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/mt168438">Settings</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the settings object for the Remote Desktop Protocol (RDP) app container client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0fe1d319-0553-46ca-8fa9-0d531a900344">TouchPointer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains the <a href="https://msdn.microsoft.com/98c47e41-ecda-45cb-94e9-de51edc7af08">RemoteDesktopClientTouchPointer</a> object for the Remote Desktop Protocol (RDP) app container client.

</td>
</tr>
</table> 


---
UID: NN:rdpappcontainerclient.IRemoteDesktopClient
title: IRemoteDesktopClient (rdpappcontainerclient.h)
description: Provides methods and properties used to configure and use the Remote Desktop Protocol (RDP) app container client control.helpviewer_keywords: ["IRemoteDesktopClient","IRemoteDesktopClient interface [Remote Desktop Services]","IRemoteDesktopClient interface [Remote Desktop Services]","described","rdpappcontainerclient/IRemoteDesktopClient","termserv.iremotedesktopclient"]
old-location: termserv\iremotedesktopclient.htm
tech.root: TermServ
ms.assetid: 4b4c1080-3ea1-4557-92d6-45a80a788071
ms.date: 12/05/2018
ms.keywords: IRemoteDesktopClient, IRemoteDesktopClient interface [Remote Desktop Services], IRemoteDesktopClient interface [Remote Desktop Services],described, rdpappcontainerclient/IRemoteDesktopClient, termserv.iremotedesktopclient
f1_keywords:
- rdpappcontainerclient/IRemoteDesktopClient
dev_langs:
- c++
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
req.lib: 
req.dll: MsTscAx.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- MsTscAx.dll
api_name:
- IRemoteDesktopClient
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRemoteDesktopClient interface


## -description



Provides methods and properties used to configure and use the Remote Desktop Protocol (RDP) app container client control.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRemoteDesktopClient</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IRemoteDesktopClient</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-attachevent">attachEvent</a>
</td>
<td align="left" width="63%">
Attaches an event handler to an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-connect">Connect</a>
</td>
<td align="left" width="63%">
Initiates a connection by using the properties currently set on the Remote Desktop Protocol (RDP) app container client control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-deletesavedcredentials">DeleteSavedCredentials</a>
</td>
<td align="left" width="63%">
Deletes saved credentials for the specified remote computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-detachevent">detachEvent</a>
</td>
<td align="left" width="63%">
Detaches an event handler from an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-disconnect">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects the active connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-reconnect">Reconnect</a>
</td>
<td align="left" width="63%">
Initiates an automatic reconnection of the Remote Desktop Protocol (RDP) app container client control to fit the session to the new width and height.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-updatesessiondisplaysettings">UpdateSessionDisplaySettings</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_actions">Actions</a>


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

<a href="https://docs.microsoft.com/windows/desktop/TermServ/iremotedesktopclient-settings">Settings</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_touchpointer">TouchPointer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains the <a href="https://docs.microsoft.com/windows/desktop/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer">RemoteDesktopClientTouchPointer</a> object for the Remote Desktop Protocol (RDP) app container client.

</td>
</tr>
</table> 


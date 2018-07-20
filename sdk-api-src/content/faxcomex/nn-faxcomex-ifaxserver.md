---
UID: NN:faxcomex.IFaxServer
title: IFaxServer
author: windows-sdk-content
description: The IFaxServer interface describes a messaging collection that is used by a fax client application to manage a connection to the fax service.
old-location: fax\_mfax_faxserver_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4isy_cpp.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IFaxServer, IFaxServer interface [Fax Service], IFaxServer interface [Fax Service],described, _mfax_faxserver_cpp, fax._mfax_faxserver_cpp, faxcomex/IFaxServer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxServer
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxServer interface


## -description


The <b>IFaxServer</b> interface describes a messaging collection that is used by a fax client application to manage a connection to the fax service. The object includes methods to create and terminate connections with a fax server, and to retrieve information about a connected fax server. The object also includes methods to store extension configuration properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxServer</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFaxServer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFaxServer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms687537(v=VS.85).aspx">Connect</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms687537(v=VS.85).aspx">IFaxServer::Connect</a> method connects a fax client application to the specified fax server.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1246897-a2a9-4750-8900-248c214d4f70">Disconnect</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b1246897-a2a9-4750-8900-248c214d4f70">IFaxServer::Disconnect</a> method terminates a fax client application's connection to a fax server. The method fails if the client is not connected to an active fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms689565(v=VS.85).aspx">GetDeviceProviders</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms689565(v=VS.85).aspx">IFaxServer::GetDeviceProviders</a> method creates a <a href="https://msdn.microsoft.com/library/ms687081(v=VS.85).aspx">IFaxDeviceProviders</a> interface, a collection of FSPs that are currently registered with the fax service. You can use the <b>IFaxDeviceProviders</b> interface to enumerate the FSPs associated with a fax server and to create and access <a href="https://msdn.microsoft.com/library/ms684893(v=VS.85).aspx">IFaxDeviceProvider</a> interfaces for them.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms689596(v=VS.85).aspx">GetDevices</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms689596(v=VS.85).aspx">IFaxServer::GetDevices</a> method creates a <a href="https://msdn.microsoft.com/library/ms684821(v=VS.85).aspx">IFaxDevices</a> interface, a collection of all the fax devices exposed by all the FSPs currently registered with the fax service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1e78db9-f59d-43de-a480-b449befc8ffc">GetExtensionProperty</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/a1e78db9-f59d-43de-a480-b449befc8ffc">IFaxServer::GetExtensionProperty</a> method retrieves an extension configuration property stored at the server level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9850a677-6ae0-4780-8655-90a8d81fe765">ListenToServerEvents</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/9850a677-6ae0-4780-8655-90a8d81fe765">IFaxServer::ListenToServerEvents</a> method registers the <a href="https://msdn.microsoft.com/library/ms689109(v=VS.85).aspx">FaxServer</a> object to receive notifications about one or more types of server events, or to stop these notifications. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/124b66b0-325c-46af-ac1f-1c75914bb6bc">RegisterDeviceProvider</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/124b66b0-325c-46af-ac1f-1c75914bb6bc">IFaxServer::RegisterDeviceProvider</a> method registers a FSP with the fax service. Registration takes place after the fax service restarts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e29d3ab2-facf-40a9-b1fa-05e1c0f3a5f1">RegisterInboundRoutingExtension</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/e29d3ab2-facf-40a9-b1fa-05e1c0f3a5f1">IFaxServer::RegisterInboundRoutingExtension</a> method registers a fax inbound routing extension with the fax service. Registration takes place after the fax service restarts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12461f0b-0c1a-4630-a881-419d829b4d42">SetExtensionProperty</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/12461f0b-0c1a-4630-a881-419d829b4d42">IFaxServer::SetExtensionProperty</a> method stores an extension configuration property at the server level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00347649-d383-4b10-8158-6b65dd299643">UnregisterDeviceProvider</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/00347649-d383-4b10-8158-6b65dd299643">IFaxServer::UnregisterDeviceProvider</a> method unregisters (removes the registration of) an existing device provider. Unregistration will take place only after the fax server is restarted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/984f0edd-23a9-481e-8377-3267b1396853">UnregisterInboundRoutingExtension</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/984f0edd-23a9-481e-8377-3267b1396853">IFaxServer::UnregisterInboundRoutingExtension</a> method unregisters an existing inbound routing extension. Unregistration will take place only after the fax server is restarted.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxServer</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/ms688482(v=VS.85).aspx">Activity</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms688482(v=VS.85).aspx">IFaxServer::get_Activity</a> property creates a <a href="https://msdn.microsoft.com/library/ms686149(v=VS.85).aspx">IFaxActivity</a> interface object. The interface permits a fax client application to access information about the activity on a connected fax server, and the fax server status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/ms689096(v=VS.85).aspx">APIVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms689096(v=VS.85).aspx">IFaxServer::get_APIVersion</a> property is a value that indicates the version of the fax server API.



</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8fc810f1-9953-4406-82c6-dda3ebfa9213">Debug</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/8fc810f1-9953-4406-82c6-dda3ebfa9213">IFaxServer::get_Debug</a> property is a Boolean value that indicates whether the fax server was created in a debug environment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/ms689198(v=VS.85).aspx">Folders</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms689198(v=VS.85).aspx">IFaxServer::get_Folders</a> property accesses a <a href="https://msdn.microsoft.com/library/ms684838(v=VS.85).aspx">IFaxFolders</a> configuration interface. You can use the interface to access the folders, jobs, and messages on a connected fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/ms688280(v=VS.85).aspx">InboundRouting</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms688280(v=VS.85).aspx">IFaxServer::get_InboundRouting</a> property creates a <a href="https://msdn.microsoft.com/library/ms684596(v=VS.85).aspx">IFaxInboundRouting</a> configuration interface. The interface permits access to an inbound fax routing extension and its methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/ms690045(v=VS.85).aspx">LoggingOptions</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms690045(v=VS.85).aspx">IFaxServer::get_LoggingOptions</a> property creates a <a href="https://msdn.microsoft.com/library/ms686873(v=VS.85).aspx">IFaxLoggingOptions</a> configuration interface. The interface permits configuration of both the activity logging options and the event logging categories that the fax service uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2e34c393-bbdc-47ce-97d7-7ae172938c05">MajorBuild</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/2e34c393-bbdc-47ce-97d7-7ae172938c05">IFaxServer::get_MajorBuild</a> property is a value that specifies the major part of the build number for the fax service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/83e0d41b-df37-4f9d-bec3-9e1b49f048b9">MajorVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/83e0d41b-df37-4f9d-bec3-9e1b49f048b9">IFaxServer::get_MajorVersion</a> property is a value that specifies the major part of the version number for the fax service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0de00fbe-ab32-4fc9-8a82-93f3abadfe2e">MinorBuild</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/0de00fbe-ab32-4fc9-8a82-93f3abadfe2e">IFaxServer::get_MinorBuild</a> property is a value that specifies the minor part of the build number for the fax service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f56f001b-5ea6-4ace-8731-34da78484658">MinorVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/f56f001b-5ea6-4ace-8731-34da78484658">IFaxServer::get_MinorVersion</a> property is a value that specifies the minor part of the version number for the fax service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/ms689567(v=VS.85).aspx">OutboundRouting</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms689567(v=VS.85).aspx">IFaxServer::get_OutboundRouting</a> property creates a <a href="https://msdn.microsoft.com/library/ms690138(v=VS.85).aspx">IFaxOutboundRouting</a> configuration interface. The interface permits users to configure outbound routing groups and rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/ms690215(v=VS.85).aspx">ReceiptOptions</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms690215(v=VS.85).aspx">IFaxServer::get_ReceiptOptions</a> property creates a <a href="https://msdn.microsoft.com/library/ms690119(v=VS.85).aspx">IFaxReceiptOptions</a> configuration interface. The object permits a fax client application to set and retrieve the receipt configuration that the fax service uses to send fax receipts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9ad7caf3-1866-4c1a-88fb-1f6f6e057a26">RegisteredEvents</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/9ad7caf3-1866-4c1a-88fb-1f6f6e057a26">IFaxServer::get_RegisteredEvents</a> property is a value from an enumeration that indicates the types of fax service events a client application is listening for.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/ms689081(v=VS.85).aspx">Security</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/ms689081(v=VS.85).aspx">IFaxServer::get_Security</a> property creates a <a href="https://msdn.microsoft.com/library/ms689510(v=VS.85).aspx">IFaxSecurity</a> configuration interface. The interface permits the calling application to set and retrieve a security descriptor for the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/mt764014">ServerName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/18efaadb-0d26-46be-b8e3-73f539a8d42b">IFaxServer::get_ServerName</a> property retrieves the name of the active fax server to which the fax client is connected.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxServer</b> is provided as the <a href="https://msdn.microsoft.com/library/ms689109(v=VS.85).aspx">FaxServer</a> object.




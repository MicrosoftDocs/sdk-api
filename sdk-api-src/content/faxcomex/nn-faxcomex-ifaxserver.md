---
UID: NN:faxcomex.IFaxServer
title: IFaxServer (faxcomex.h)

description: The IFaxServer interface describes a messaging collection that is used by a fax client application to manage a connection to the fax service.
old-location: fax\_mfax_faxserver_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4isy_cpp.htm

ms.date: 12/05/2018
ms.keywords: IFaxServer, IFaxServer interface [Fax Service], IFaxServer interface [Fax Service],described, _mfax_faxserver_cpp, fax._mfax_faxserver_cpp, faxcomex/IFaxServer
ms.topic: interface
f1_keywords: 
 - "faxcomex/IFaxServer"
dev_langs:
 - c++
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxServer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxServer interface


## -description


The <b>IFaxServer</b> interface describes a messaging collection that is used by a fax client application to manage a connection to the fax service. The object includes methods to create and terminate connections with a fax server, and to retrieve information about a connected fax server. The object also includes methods to store extension configuration properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFaxServer</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFaxServer</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-connect-vb">Connect</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-connect-vb">IFaxServer::Connect</a> method connects a fax client application to the specified fax server.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-disconnect-vb">Disconnect</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-disconnect-vb">IFaxServer::Disconnect</a> method terminates a fax client application's connection to a fax server. The method fails if the client is not connected to an active fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-getdeviceproviders">GetDeviceProviders</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-getdeviceproviders">IFaxServer::GetDeviceProviders</a> method creates a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceproviders">IFaxDeviceProviders</a> interface, a collection of FSPs that are currently registered with the fax service. You can use the <b>IFaxDeviceProviders</b> interface to enumerate the FSPs associated with a fax server and to create and access <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceprovider">IFaxDeviceProvider</a> interfaces for them.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-getdevices">GetDevices</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-getdevices">IFaxServer::GetDevices</a> method creates a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdevices">IFaxDevices</a> interface, a collection of all the fax devices exposed by all the FSPs currently registered with the fax service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-getextensionproperty-vb">GetExtensionProperty</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-getextensionproperty-vb">IFaxServer::GetExtensionProperty</a> method retrieves an extension configuration property stored at the server level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-listentoserverevents-vb">ListenToServerEvents</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-listentoserverevents-vb">IFaxServer::ListenToServerEvents</a> method registers the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a> object to receive notifications about one or more types of server events, or to stop these notifications. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-registerdeviceprovider-vb">RegisterDeviceProvider</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-registerdeviceprovider-vb">IFaxServer::RegisterDeviceProvider</a> method registers a FSP with the fax service. Registration takes place after the fax service restarts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-registerinboundroutingextension-vb">RegisterInboundRoutingExtension</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-registerinboundroutingextension-vb">IFaxServer::RegisterInboundRoutingExtension</a> method registers a fax inbound routing extension with the fax service. Registration takes place after the fax service restarts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-setextensionproperty-vb">SetExtensionProperty</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-setextensionproperty-vb">IFaxServer::SetExtensionProperty</a> method stores an extension configuration property at the server level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-unregisterdeviceprovider-vb">UnregisterDeviceProvider</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-unregisterdeviceprovider-vb">IFaxServer::UnregisterDeviceProvider</a> method unregisters (removes the registration of) an existing device provider. Unregistration will take place only after the fax server is restarted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-unregisterinboundroutingextension-vb">UnregisterInboundRoutingExtension</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-unregisterinboundroutingextension-vb">IFaxServer::UnregisterInboundRoutingExtension</a> method unregisters an existing inbound routing extension. Unregistration will take place only after the fax server is restarted.

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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-get_activity">Activity</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-get_activity">IFaxServer::get_Activity</a> property creates a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxactivity">IFaxActivity</a> interface object. The interface permits a fax client application to access information about the activity on a connected fax server, and the fax server status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-apiversion-vb">APIVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-apiversion-vb">IFaxServer::get_APIVersion</a> property is a value that indicates the version of the fax server API.



</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-debug-vb">Debug</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-debug-vb">IFaxServer::get_Debug</a> property is a Boolean value that indicates whether the fax server was created in a debug environment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-get_folders">Folders</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-get_folders">IFaxServer::get_Folders</a> property accesses a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxfolders">IFaxFolders</a> configuration interface. You can use the interface to access the folders, jobs, and messages on a connected fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-get_inboundrouting">InboundRouting</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-get_inboundrouting">IFaxServer::get_InboundRouting</a> property creates a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxinboundrouting">IFaxInboundRouting</a> configuration interface. The interface permits access to an inbound fax routing extension and its methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-get_loggingoptions">LoggingOptions</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-get_loggingoptions">IFaxServer::get_LoggingOptions</a> property creates a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxloggingoptions">IFaxLoggingOptions</a> configuration interface. The interface permits configuration of both the activity logging options and the event logging categories that the fax service uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-majorbuild-vb">MajorBuild</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-majorbuild-vb">IFaxServer::get_MajorBuild</a> property is a value that specifies the major part of the build number for the fax service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-majorversion-vb">MajorVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-majorversion-vb">IFaxServer::get_MajorVersion</a> property is a value that specifies the major part of the version number for the fax service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-minorbuild-vb">MinorBuild</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-minorbuild-vb">IFaxServer::get_MinorBuild</a> property is a value that specifies the minor part of the build number for the fax service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-minorversion-vb">MinorVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-minorversion-vb">IFaxServer::get_MinorVersion</a> property is a value that specifies the minor part of the version number for the fax service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-get_outboundrouting">OutboundRouting</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-get_outboundrouting">IFaxServer::get_OutboundRouting</a> property creates a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundrouting">IFaxOutboundRouting</a> configuration interface. The interface permits users to configure outbound routing groups and rules.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-get_receiptoptions">ReceiptOptions</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-get_receiptoptions">IFaxServer::get_ReceiptOptions</a> property creates a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxreceiptoptions">IFaxReceiptOptions</a> configuration interface. The object permits a fax client application to set and retrieve the receipt configuration that the fax service uses to send fax receipts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-registeredevents-vb">RegisteredEvents</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-registeredevents-vb">IFaxServer::get_RegisteredEvents</a> property is a value from an enumeration that indicates the types of fax service events a client application is listening for.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-get_security">Security</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxserver-get_security">IFaxServer::get_Security</a> property creates a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxsecurity">IFaxSecurity</a> configuration interface. The interface permits the calling application to set and retrieve a security descriptor for the fax server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-servername-vb">ServerName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-servername-vb">IFaxServer::get_ServerName</a> property retrieves the name of the active fax server to which the fax client is connected.

</td>
</tr>
</table> 


## -remarks



A default implementation of <b>IFaxServer</b> is provided as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver">FaxServer</a> object.




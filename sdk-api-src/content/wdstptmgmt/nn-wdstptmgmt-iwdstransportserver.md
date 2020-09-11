---
UID: NN:wdstptmgmt.IWdsTransportServer
title: IWdsTransportServer (wdstptmgmt.h)
description: Represents a WDS transport server. A WDS client can use an object of this interface to manage setup, configuration, and namespace tasks on the server.
helpviewer_keywords: ["IWdsTransportServer","IWdsTransportServer interface [Windows Deployment Services]","IWdsTransportServer interface [Windows Deployment Services]","described","wds.iwdstransportserver","wdstptmgmt/IWdsTransportServer"]
old-location: wds\iwdstransportserver.htm
tech.root: wds
ms.assetid: 0129658d-8725-4020-ae9c-9d0a44075561
ms.date: 12/05/2018
ms.keywords: IWdsTransportServer, IWdsTransportServer interface [Windows Deployment Services], IWdsTransportServer interface [Windows Deployment Services],described, wds.iwdstransportserver, wdstptmgmt/IWdsTransportServer
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wdstptmgmt.tlb
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWdsTransportServer
 - wdstptmgmt/IWdsTransportServer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportServer
---

# IWdsTransportServer interface


## -description

Represents a  WDS transport server.  A WDS client can use an object of this interface to manage setup, configuration, and namespace tasks on the server.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportServer</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWdsTransportServer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWdsTransportServer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportserver-disconnectclient">DisconnectClient</a>
</td>
<td align="left" width="63%">
Disconnects a WDS client from a transport session and specifies what action the WDS client should take upon disconnection. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportServer</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportserver-get_configurationmanager">ConfigurationManager</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a pointer to the object of an <a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportconfigurationmanager">IWdsTransportConfigurationManager</a> interface used to manage the configuration of this server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportserver-get_name">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the name of the server represented by this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportserver-get_namespacemanager">NamespaceManager</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a pointer to the object of an  <a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespacemanager">IWdsTransportNamespaceManager</a> interface used to manage namespaces on this server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportserver-get_setupmanager">SetupManager</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a pointer to the object of an  <a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportsetupmanager">IWdsTransportSetupManager</a> interface used to manage setup functionality on this server.

</td>
</tr>
</table>


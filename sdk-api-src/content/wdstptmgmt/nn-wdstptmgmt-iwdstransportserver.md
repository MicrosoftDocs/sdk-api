---
UID: NN:wdstptmgmt.IWdsTransportServer
title: IWdsTransportServer
author: windows-sdk-content
description: Represents a WDS transport server. A WDS client can use an object of this interface to manage setup, configuration, and namespace tasks on the server.
old-location: wds\iwdstransportserver.htm
old-project: Wds
ms.assetid: 0129658d-8725-4020-ae9c-9d0a44075561
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWdsTransportServer, IWdsTransportServer interface [Windows Deployment Services], IWdsTransportServer interface [Windows Deployment Services],described, wds.iwdstransportserver, wdstptmgmt/IWdsTransportServer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wdstptmgmt.dll
api_name:
-	IWdsTransportServer
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWdsTransportServer interface


## -description


Represents a  WDS transport server.  A WDS client can use an object of this interface to manage setup, configuration, and namespace tasks on the server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportServer</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWdsTransportServer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7ab63f7e-1840-40d1-8933-ea92042aaced">DisconnectClient</a>
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

<a href="https://msdn.microsoft.com/007e166b-a8f9-4acc-8963-ffa14b22084a">ConfigurationManager</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a pointer to the object of an <a href="https://msdn.microsoft.com/b86f9bc7-ddee-4d18-b5cb-28d28fa7ae7e">IWdsTransportConfigurationManager</a> interface used to manage the configuration of this server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


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

<a href="https://msdn.microsoft.com/3f54d5ef-c630-4f5b-93ea-1da7303482ba">NamespaceManager</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a pointer to the object of an  <a href="https://msdn.microsoft.com/de5fc470-af9f-4f9f-bc17-a347dc702e36">IWdsTransportNamespaceManager</a> interface used to manage namespaces on this server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/17bd15d2-5468-4e8e-8d1f-d4b17a27be2f">SetupManager</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a pointer to the object of an  <a href="https://msdn.microsoft.com/b7b0dc9f-081e-472f-98f7-fe555a411ea3">IWdsTransportSetupManager</a> interface used to manage setup functionality on this server.

</td>
</tr>
</table> 


---
UID: NN:wdstptmgmt.IWdsTransportContent
title: IWdsTransportContent
author: windows-sdk-content
description: Represents content being transmitted under a namespace over one or more sessions.
old-location: wds\iwdstransportcontent.htm
old-project: Wds
ms.assetid: d7ed1f64-578f-4b3a-b9af-9a48800b9ca4
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWdsTransportContent, IWdsTransportContent interface [Windows Deployment Services], IWdsTransportContent interface [Windows Deployment Services],described, wds.iwdstransportcontent, wdstptmgmt/IWdsTransportContent
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
tech.root: 
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportContent
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWdsTransportContent interface


## -description


Represents content being transmitted under a namespace over one or more sessions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportContent</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWdsTransportContent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWdsTransportContent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8901f9c5-931e-40d5-8a5c-d3a814556400">RetrieveSessions</a>
</td>
<td align="left" width="63%">
Retrieves a collection of active transport sessions associated with this content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bcc4359f-0536-4cd4-a937-37d4e69ab497">Terminate</a>
</td>
<td align="left" width="63%">
Terminates the transmission of this content by terminating all active sessions under the content and disconnecting any clients that are joined to them.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportContent</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn895599">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the unique content ID that identifies this content object on the server.

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
Receives a pointer to a string value that contains the name of the data object represented by this content object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8b116f8d-bcbc-4313-9527-07f871e00842">Namespace</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a pointer to an object of an  <a href="https://msdn.microsoft.com/eadb7b1b-aaef-4a4e-a2de-c641a4e10173">IWdsTransportNamespace</a> interface that represents the namespace associated with this content.

</td>
</tr>
</table> 


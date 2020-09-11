---
UID: NN:wdstptmgmt.IWdsTransportContent
title: IWdsTransportContent (wdstptmgmt.h)
description: Represents content being transmitted under a namespace over one or more sessions.
helpviewer_keywords: ["IWdsTransportContent","IWdsTransportContent interface [Windows Deployment Services]","IWdsTransportContent interface [Windows Deployment Services]","described","wds.iwdstransportcontent","wdstptmgmt/IWdsTransportContent"]
old-location: wds\iwdstransportcontent.htm
tech.root: wds
ms.assetid: d7ed1f64-578f-4b3a-b9af-9a48800b9ca4
ms.date: 12/05/2018
ms.keywords: IWdsTransportContent, IWdsTransportContent interface [Windows Deployment Services], IWdsTransportContent interface [Windows Deployment Services],described, wds.iwdstransportcontent, wdstptmgmt/IWdsTransportContent
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
 - IWdsTransportContent
 - wdstptmgmt/IWdsTransportContent
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
 - IWdsTransportContent
---

# IWdsTransportContent interface


## -description

Represents content being transmitted under a namespace over one or more sessions.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportContent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWdsTransportContent</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportcontent-retrievesessions">RetrieveSessions</a>
</td>
<td align="left" width="63%">
Retrieves a collection of active transport sessions associated with this content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportcontent-terminate">Terminate</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportcontent-get_id">Id</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportcontent-get_name">Name</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportcontent-get_namespace">Namespace</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a pointer to an object of an  <a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportnamespace">IWdsTransportNamespace</a> interface that represents the namespace associated with this content.

</td>
</tr>
</table>


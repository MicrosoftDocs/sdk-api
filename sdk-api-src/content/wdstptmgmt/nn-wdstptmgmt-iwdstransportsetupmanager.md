---
UID: NN:wdstptmgmt.IWdsTransportSetupManager
title: IWdsTransportSetupManager (wdstptmgmt.h)
description: Manages setup tasks on a WDS transport server.
helpviewer_keywords: ["IWdsTransportSetupManager","IWdsTransportSetupManager interface [Windows Deployment Services]","IWdsTransportSetupManager interface [Windows Deployment Services]","described","wds.iwdstransportsetupmanager","wdstptmgmt/IWdsTransportSetupManager"]
old-location: wds\iwdstransportsetupmanager.htm
tech.root: wds
ms.assetid: b7b0dc9f-081e-472f-98f7-fe555a411ea3
ms.date: 12/05/2018
ms.keywords: IWdsTransportSetupManager, IWdsTransportSetupManager interface [Windows Deployment Services], IWdsTransportSetupManager interface [Windows Deployment Services],described, wds.iwdstransportsetupmanager, wdstptmgmt/IWdsTransportSetupManager
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
 - IWdsTransportSetupManager
 - wdstptmgmt/IWdsTransportSetupManager
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
 - IWdsTransportSetupManager
---

# IWdsTransportSetupManager interface


## -description

Manages setup tasks on a WDS transport server.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportSetupManager</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWdsTransportSetupManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWdsTransportSetupManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportsetupmanager-deregistercontentprovider">DeregisterContentProvider</a>
</td>
<td align="left" width="63%">
Deregisters a content provider DLL from use by the WDS transport server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportsetupmanager-registercontentprovider">RegisterContentProvider</a>
</td>
<td align="left" width="63%">
Registers a content provider DLL for use by the WDS transport server.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportSetupManager</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportsetupmanager-get_installedfeatures">InstalledFeatures</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a value that indicates which WDS features are installed on the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportsetupmanager-get_protocols">Protocols</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a value that indicates which transport protocols are supported by the WDS server. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportsetupmanager-get_version">Version</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a value that indicates the operating system version of the WDS server.

</td>
</tr>
</table>
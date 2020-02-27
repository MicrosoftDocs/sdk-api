---
UID: NN:wdstptmgmt.IWdsTransportClient
title: IWdsTransportClient (wdstptmgmt.h)
description: Represents a WDS client that is joined to a transport session on a WDS transport server.
old-location: wds\iwdstransportclient.htm
tech.root: wds
ms.assetid: 39534411-3d69-408d-b495-10851fe40bdf
ms.date: 12/05/2018
ms.keywords: IWdsTransportClient, IWdsTransportClient interface [Windows Deployment Services], IWdsTransportClient interface [Windows Deployment Services],described, wds.iwdstransportclient, wdstptmgmt/IWdsTransportClient
f1_keywords:
- wdstptmgmt/IWdsTransportClient
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wdstptmgmt.dll
api_name:
- IWdsTransportClient
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWdsTransportClient interface


## -description


Represents a WDS client that is joined to a transport session on a  WDS transport server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportClient</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWdsTransportClient</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWdsTransportClient</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportclient-disconnect">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects the WDS client from the session and specifies what action the client should take upon disconnection. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportClient</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportclient-get_cpuutilization">CpuUtilization</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the percentage of the WDS client’s CPU utilization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportclient-get_id">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a unique client ID that identifies this WDS client on the WDS server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportclient-get_ipaddress">IpAddress</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a string value that contains the IP address of the WDS client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportclient-get_joinduration">JoinDuration</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the time elapsed, in seconds, since the application joined to the current session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportclient-get_macaddress">MacAddress</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the  MAC address of the WDS client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportclient-get_cpuutilization">MemoryUtilization</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the percentage of the WDS client’s memory in use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportclient-get_name">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the name of the WDS client on the WDS server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportclient-get_networkutilization">NetworkUtilization</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the percentage of the WDS client’s network bandwidth used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportclient-get_percentcompletion">PercentCompletion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the percentage of the current object that has been downloaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportclient-get_session">Session</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives the transport session to which the WDS client is joined.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nf-wdstptmgmt-iwdstransportclient-get_useridentity">UserIdentity</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a string representing the user identity associated with this client.

</td>
</tr>
</table> 


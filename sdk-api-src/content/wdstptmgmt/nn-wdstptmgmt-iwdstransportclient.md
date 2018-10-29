---
UID: NN:wdstptmgmt.IWdsTransportClient
title: IWdsTransportClient
author: windows-sdk-content
description: Represents a WDS client that is joined to a transport session on a WDS transport server.
old-location: wds\iwdstransportclient.htm
tech.root: Wds
ms.assetid: 39534411-3d69-408d-b495-10851fe40bdf
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IWdsTransportClient, IWdsTransportClient interface [Windows Deployment Services], IWdsTransportClient interface [Windows Deployment Services],described, wds.iwdstransportclient, wdstptmgmt/IWdsTransportClient
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWdsTransportClient interface


## -description


Represents a WDS client that is joined to a transport session on a  WDS transport server.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportClient</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWdsTransportClient</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/faf3ab18-2629-402f-96ad-41337c165fba">Disconnect</a>
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

<a href="https://msdn.microsoft.com/515845b9-6f5e-436f-a2f1-4963909d4071">CpuUtilization</a>


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

<a href="https://msdn.microsoft.com/3a19e711-ea4a-4b9d-b9ef-30dcd1c42d4e">Id</a>


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

<a href="https://msdn.microsoft.com/1e2d0da1-9362-4187-9ccc-80522d109c83">IpAddress</a>


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

<a href="https://msdn.microsoft.com/f9c71b00-fd76-4b02-95b3-1f930bc8e935">JoinDuration</a>


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

<a href="https://msdn.microsoft.com/cc05d24a-54c8-40e7-85e4-640813538116">MacAddress</a>


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

<a href="https://msdn.microsoft.com/515845b9-6f5e-436f-a2f1-4963909d4071">MemoryUtilization</a>


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

<a href="https://msdn.microsoft.com/e0517a4e-5312-4663-955d-1a2892492308">Name</a>


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

<a href="https://msdn.microsoft.com/feeab5f0-b549-46bc-b19d-94ab3778838c">NetworkUtilization</a>


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

<a href="https://msdn.microsoft.com/7d093d69-822c-4b89-893c-d9b070bd8133">PercentCompletion</a>


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

<a href="https://msdn.microsoft.com/19aac2c4-c724-493f-a4e9-a396a1d32f15">Session</a>


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

<a href="https://msdn.microsoft.com/c22a49ba-2f90-4131-8cf0-aa0d242d32c7">UserIdentity</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Receives a string representing the user identity associated with this client.

</td>
</tr>
</table> 


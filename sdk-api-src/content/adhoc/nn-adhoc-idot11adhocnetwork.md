---
UID: NN:adhoc.IDot11AdHocNetwork
title: IDot11AdHocNetwork
author: windows-driver-content
description: Represents an available ad hoc network destination within connection range.
old-location: nwifi\idot11adhocnetwork.htm
old-project: NativeWiFi
ms.assetid: 2736bb81-b66f-4c09-8c76-ca16f3eab192
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IDot11AdHocNetwork, IDot11AdHocNetwork interface [NativeWIFI], IDot11AdHocNetwork interface [NativeWIFI], described, adhoc/IDot11AdHocNetwork, nwifi.idot11adhocnetwork
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	adhoc.h
api_name:
-	IDot11AdHocNetwork
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDot11AdHocNetwork interface


## -description


The <b>IDot11AdHocNetwork</b> interface represents an available ad hoc network destination within connection range. Before an application can connect to a network, the network must have been created using <a href="https://msdn.microsoft.com/1d9930b3-7bc4-4015-b096-a21fe01f54f5">IDot11AdHocManager::CreateNetwork</a> and committed using <a href="https://msdn.microsoft.com/45beb340-1c19-4b91-8e5c-8849e690e988">IDot11AdHocManager::CommitCreatedNetwork</a>.
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="https://msdn.microsoft.com/library/windows/hardware/mt244265">Wi-Fi Direct</a> instead.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDot11AdHocNetwork</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDot11AdHocNetwork</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDot11AdHocNetwork</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3272e0fe-0844-4e02-bd5f-a1e1c656074d">IDot11AdHocNetwork::Connect</a>
</td>
<td align="left" width="63%">
Connects to a previously created wireless ad hoc network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f2c007c-4d24-44d7-be30-0fa7c5fbce4a">IDot11AdHocNetwork::DeleteProfile</a>
</td>
<td align="left" width="63%">
Deletes any profile associated with the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5c96776-6bb2-43b0-86b9-c3bc058d5d84">IDot11AdHocNetwork::Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects from an ad hoc network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a7e7a75-b070-4d57-ae88-6bfc3568c3c9">IDot11AdHocNetwork::GetContextGuid</a>
</td>
<td align="left" width="63%">
Gets the context identifier associated with the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c14c7fd-625b-48f7-b404-50da0db170f9">IDot11AdHocNetwork::GetInterface</a>
</td>
<td align="left" width="63%">
Gets the interface associated with a network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abd25741-25ad-4109-a07e-4146824695b5">IDot11AdHocNetwork::GetProfileName</a>
</td>
<td align="left" width="63%">
Gets the profile name associated with the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e5fa757-41fd-4541-a16e-15c2fb66e15a">IDot11AdHocNetwork::GetSecuritySetting</a>
</td>
<td align="left" width="63%">
Gets the security settings for the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be31a2ed-c9ba-4894-a295-a88e01639891">IDot11AdHocNetwork::GetSignalQuality</a>
</td>
<td align="left" width="63%">
Gets the signal quality values associated with the network's radio.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a59a8bd-d2eb-48c6-8480-dc4dea335d22">IDot11AdHocNetwork::GetSignature</a>
</td>
<td align="left" width="63%">
Gets the unique signature associated with the ad hoc network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1a190a2-038b-4353-8dc9-76950b1da9ff">IDot11AdHocNetwork::GetSSID</a>
</td>
<td align="left" width="63%">
Gets the SSID of the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd627a36-92b7-478b-8fd5-c328b8e54924">IDot11AdHocNetwork::GetStatus</a>
</td>
<td align="left" width="63%">
Gets the connection status of the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/252f32ef-0a54-445f-94ca-113a67a3e6dd">IDot11AdHocNetwork::HasProfile</a>
</td>
<td align="left" width="63%">
Returns a boolean value that specifies whether there is a saved profile associated with the network.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dcb93b9c-3292-4cbf-9d44-5367bdbd4878">IDot11AdHocManager</a>
 

 


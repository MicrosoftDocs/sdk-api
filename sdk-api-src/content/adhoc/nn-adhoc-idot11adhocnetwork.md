---
UID: NN:adhoc.IDot11AdHocNetwork
title: IDot11AdHocNetwork (adhoc.h)
description: Represents an available ad hoc network destination within connection range.
helpviewer_keywords: ["IDot11AdHocNetwork","IDot11AdHocNetwork interface [NativeWIFI]","IDot11AdHocNetwork interface [NativeWIFI]","described","adhoc/IDot11AdHocNetwork","nwifi.idot11adhocnetwork"]
old-location: nwifi\idot11adhocnetwork.htm
tech.root: nwifi
ms.assetid: 2736bb81-b66f-4c09-8c76-ca16f3eab192
ms.date: 12/05/2018
ms.keywords: IDot11AdHocNetwork, IDot11AdHocNetwork interface [NativeWIFI], IDot11AdHocNetwork interface [NativeWIFI],described, adhoc/IDot11AdHocNetwork, nwifi.idot11adhocnetwork
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDot11AdHocNetwork
 - adhoc/IDot11AdHocNetwork
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocNetwork
---

# IDot11AdHocNetwork interface


## -description

The <b>IDot11AdHocNetwork</b> interface represents an available ad hoc network destination within connection range. Before an application can connect to a network, the network must have been created using <a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocmanager-createnetwork">IDot11AdHocManager::CreateNetwork</a> and committed using <a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocmanager-commitcreatednetwork">IDot11AdHocManager::CommitCreatedNetwork</a>.
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="https://docs.microsoft.com/windows/desktop/NativeWiFi/about-the-wi-fi-direct-api">Wi-Fi Direct</a> instead.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDot11AdHocNetwork</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDot11AdHocNetwork</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocnetwork-connect">IDot11AdHocNetwork::Connect</a>
</td>
<td align="left" width="63%">
Connects to a previously created wireless ad hoc network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocnetwork-deleteprofile">IDot11AdHocNetwork::DeleteProfile</a>
</td>
<td align="left" width="63%">
Deletes any profile associated with the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocnetwork-disconnect">IDot11AdHocNetwork::Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects from an ad hoc network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocnetwork-getcontextguid">IDot11AdHocNetwork::GetContextGuid</a>
</td>
<td align="left" width="63%">
Gets the context identifier associated with the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocnetwork-getinterface">IDot11AdHocNetwork::GetInterface</a>
</td>
<td align="left" width="63%">
Gets the interface associated with a network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocnetwork-getprofilename">IDot11AdHocNetwork::GetProfileName</a>
</td>
<td align="left" width="63%">
Gets the profile name associated with the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocnetwork-getsecuritysetting">IDot11AdHocNetwork::GetSecuritySetting</a>
</td>
<td align="left" width="63%">
Gets the security settings for the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocnetwork-getsignalquality">IDot11AdHocNetwork::GetSignalQuality</a>
</td>
<td align="left" width="63%">
Gets the signal quality values associated with the network's radio.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocnetwork-getsignature">IDot11AdHocNetwork::GetSignature</a>
</td>
<td align="left" width="63%">
Gets the unique signature associated with the ad hoc network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocnetwork-getssid">IDot11AdHocNetwork::GetSSID</a>
</td>
<td align="left" width="63%">
Gets the SSID of the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocnetwork-getstatus">IDot11AdHocNetwork::GetStatus</a>
</td>
<td align="left" width="63%">
Gets the connection status of the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocnetwork-hasprofile">IDot11AdHocNetwork::HasProfile</a>
</td>
<td align="left" width="63%">
Returns a boolean value that specifies whether there is a saved profile associated with the network.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager">IDot11AdHocManager</a>


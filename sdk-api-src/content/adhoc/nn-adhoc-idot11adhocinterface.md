---
UID: NN:adhoc.IDot11AdHocInterface
title: IDot11AdHocInterface
author: windows-sdk-content
description: Represents a wireless network interface card (NIC).
old-location: nwifi\idot11adhocinterface.htm
old-project: nativewifi
ms.assetid: a4a73ff8-e24a-4f44-9205-c60699d1c27d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDot11AdHocInterface, IDot11AdHocInterface interface [NativeWIFI], IDot11AdHocInterface interface [NativeWIFI],described, adhoc/IDot11AdHocInterface, nwifi.idot11adhocinterface
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocInterface
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDot11AdHocInterface interface


## -description


Represents a wireless network interface card (NIC).
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="https://msdn.microsoft.com/library/windows/hardware/mt244265">Wi-Fi Direct</a> instead.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDot11AdHocInterface</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDot11AdHocInterface</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDot11AdHocInterface</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aefe605a-720d-40da-8d0f-b1d5dd5b306e">IDot11AdHocInterface::GetActiveNetwork</a>
</td>
<td align="left" width="63%">
Gets the network that is currently active on the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d65fe0ae-ce7b-4d9e-af5b-d9aaeb909e21">IDot11AdHocInterface::GetDeviceSignature</a>
</td>
<td align="left" width="63%">
Gets the signature of the NIC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/945947e9-99ea-4420-95db-5b831e59e894">IDot11AdHocInterface::GetFriendlyName</a>
</td>
<td align="left" width="63%">
Gets the friendly name of the NIC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/997acc8d-a4e7-43dc-917d-7a2b69f3c049">IDot11AdHocInterface::GetIEnumDot11AdHocNetworks</a>
</td>
<td align="left" width="63%">
Gets the collection of networks associated with this NIC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5f98222-83aa-4ba9-adc7-e7b67eb5dc0d">IDot11AdHocInterface::GetIEnumSecuritySettings</a>
</td>
<td align="left" width="63%">
Gets the collection of security settings associated with this NIC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54e271dc-b710-4229-9682-2919af6cd998">IDot11AdHocInterface::GetStatus</a>
</td>
<td align="left" width="63%">
Gets the connection status of the network associated with this NIC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18e3419f-500e-40bb-b7f1-125e95c55690">IDot11AdHocInterface::IsAdHocCapable</a>
</td>
<td align="left" width="63%">
Specifies whether a NIC supports the  creation or use of an ad hoc network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3854b2e3-853d-44cd-9b43-6c583f0df08f">IDot11AdHocInterface::IsDot11d</a>
</td>
<td align="left" width="63%">
Specifies whether the NIC is 802.11d compliant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5d76166-b960-4b70-acf7-e8eb65ca8cfb">IDot11AdHocInterface::IsRadioOn</a>
</td>
<td align="left" width="63%">
Specifies whether the radio is on.

</td>
</tr>
</table> 


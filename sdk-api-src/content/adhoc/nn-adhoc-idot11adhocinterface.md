---
UID: NN:adhoc.IDot11AdHocInterface
title: IDot11AdHocInterface (adhoc.h)

description: Represents a wireless network interface card (NIC).
old-location: nwifi\idot11adhocinterface.htm
tech.root: NativeWiFi
ms.assetid: a4a73ff8-e24a-4f44-9205-c60699d1c27d

ms.date: 12/05/2018
ms.keywords: IDot11AdHocInterface, IDot11AdHocInterface interface [NativeWIFI], IDot11AdHocInterface interface [NativeWIFI],described, adhoc/IDot11AdHocInterface, nwifi.idot11adhocinterface
ms.topic: interface
f1_keywords: 
 - "adhoc/IDot11AdHocInterface"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocInterface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDot11AdHocInterface interface


## -description


Represents a wireless network interface card (NIC).
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="https://docs.microsoft.com/windows/desktop/NativeWiFi/about-the-wi-fi-direct-api">Wi-Fi Direct</a> instead.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDot11AdHocInterface</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDot11AdHocInterface</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocinterface-getactivenetwork">IDot11AdHocInterface::GetActiveNetwork</a>
</td>
<td align="left" width="63%">
Gets the network that is currently active on the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocinterface-getdevicesignature">IDot11AdHocInterface::GetDeviceSignature</a>
</td>
<td align="left" width="63%">
Gets the signature of the NIC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocinterface-getfriendlyname">IDot11AdHocInterface::GetFriendlyName</a>
</td>
<td align="left" width="63%">
Gets the friendly name of the NIC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocinterface-getienumdot11adhocnetworks">IDot11AdHocInterface::GetIEnumDot11AdHocNetworks</a>
</td>
<td align="left" width="63%">
Gets the collection of networks associated with this NIC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocinterface-getienumsecuritysettings">IDot11AdHocInterface::GetIEnumSecuritySettings</a>
</td>
<td align="left" width="63%">
Gets the collection of security settings associated with this NIC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocinterface-getstatus">IDot11AdHocInterface::GetStatus</a>
</td>
<td align="left" width="63%">
Gets the connection status of the network associated with this NIC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocinterface-isadhoccapable">IDot11AdHocInterface::IsAdHocCapable</a>
</td>
<td align="left" width="63%">
Specifies whether a NIC supports the  creation or use of an ad hoc network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocinterface-isdot11d">IDot11AdHocInterface::IsDot11d</a>
</td>
<td align="left" width="63%">
Specifies whether the NIC is 802.11d compliant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-idot11adhocinterface-isradioon">IDot11AdHocInterface::IsRadioOn</a>
</td>
<td align="left" width="63%">
Specifies whether the radio is on.

</td>
</tr>
</table> 


---
UID: NN:mbnapi.IMbnRegistration
title: IMbnRegistration (mbnapi.h)
description: Provides access to network registration data.
old-location: mbn\imbnregistration.htm
tech.root: mbn
ms.assetid: da5413b7-adf4-4a3d-893f-f51441460541
ms.date: 12/05/2018
ms.keywords: IMbnRegistration, IMbnRegistration interface [Microsoft Broadband Networks], IMbnRegistration interface [Microsoft Broadband Networks],described, mbn.imbnregistration, mbnapi/IMbnRegistration
f1_keywords:
- mbnapi/IMbnRegistration
dev_langs:
- c++
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
- mbnapi.h
api_name:
- IMbnRegistration
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnRegistration interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Provides access to network registration data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnRegistration</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistration-getavailabledataclasses">GetAvailableDataClasses</a>
</td>
<td align="left" width="63%">
Gets the available data classes in the current network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistration-getcurrentdataclass">GetCurrentDataClass</a>
</td>
<td align="left" width="63%">
Gets the current data class in the current network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistration-getpacketattachnetworkerror">GetPacketAttachNetworkError</a>
</td>
<td align="left" width="63%">
Gets the network error from a packet attach operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistration-getproviderid">GetProviderID</a>
</td>
<td align="left" width="63%">
Gets the provider ID for the currently registered network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistration-getprovidername">GetProviderName</a>
</td>
<td align="left" width="63%">
Gets the provider name for the currently registered network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistration-getregistermode">GetRegisterMode</a>
</td>
<td align="left" width="63%">
Gets the network registration mode of an Mobile Broadband device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistration-getregisterstate">GetRegisterState</a>
</td>
<td align="left" width="63%">
Gets the registration state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistration-getregistrationnetworkerror">GetRegistrationNetworkError</a>
</td>
<td align="left" width="63%">
Gets the network error from a registration operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistration-getroamingtext">GetRoamingText</a>
</td>
<td align="left" width="63%">
Gets the roaming text describing the roaming provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnregistration-setregistermode">SetRegisterMode</a>
</td>
<td align="left" width="63%">
Sets the registration mode for the device.

</td>
</tr>
</table> 


## -remarks



An application can acquire this interface by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method of <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>.




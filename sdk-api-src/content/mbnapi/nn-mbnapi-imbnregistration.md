---
UID: NN:mbnapi.IMbnRegistration
title: IMbnRegistration (mbnapi.h)
author: windows-sdk-content
description: Provides access to network registration data.
old-location: mbn\imbnregistration.htm
tech.root: mbn
ms.assetid: da5413b7-adf4-4a3d-893f-f51441460541
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMbnRegistration, IMbnRegistration interface [Microsoft Broadband Networks], IMbnRegistration interface [Microsoft Broadband Networks],described, mbn.imbnregistration, mbnapi/IMbnRegistration
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnRegistration interface


## -description


Provides access to network registration data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnRegistration</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnRegistration</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/fb799232-0ef5-4fbd-9b7f-a106ef440a68">GetAvailableDataClasses</a>
</td>
<td align="left" width="63%">
Gets the available data classes in the current network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/365458a4-74df-4283-94db-3d855acadffe">GetCurrentDataClass</a>
</td>
<td align="left" width="63%">
Gets the current data class in the current network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b51103fe-f4b2-46a5-9335-44bf6591e447">GetPacketAttachNetworkError</a>
</td>
<td align="left" width="63%">
Gets the network error from a packet attach operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b21a103-2b49-4d99-8041-c9da9cbc5750">GetProviderID</a>
</td>
<td align="left" width="63%">
Gets the provider ID for the currently registered network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6cf7cb2-5563-49dc-ac2a-6343ae2395b2">GetProviderName</a>
</td>
<td align="left" width="63%">
Gets the provider name for the currently registered network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30030eb8-3b08-4583-a7ba-0560db32007f">GetRegisterMode</a>
</td>
<td align="left" width="63%">
Gets the network registration mode of an Mobile Broadband device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19488f2e-0cec-4e87-a32a-274e82cd8766">GetRegisterState</a>
</td>
<td align="left" width="63%">
Gets the registration state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0e6df7a-7b47-4587-92c2-f01fd96e768f">GetRegistrationNetworkError</a>
</td>
<td align="left" width="63%">
Gets the network error from a registration operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2911387-7497-43c5-bc1c-db093f31186c">GetRoamingText</a>
</td>
<td align="left" width="63%">
Gets the roaming text describing the roaming provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71434e46-7055-4721-8cc9-140e196b6097">SetRegisterMode</a>
</td>
<td align="left" width="63%">
Sets the registration mode for the device.

</td>
</tr>
</table> 


## -remarks



An application can acquire this interface by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> method of <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>.




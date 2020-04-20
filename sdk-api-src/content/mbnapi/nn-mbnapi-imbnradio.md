---
UID: NN:mbnapi.IMbnRadio
title: IMbnRadio (mbnapi.h)
description: The IMbnRadio interface is used to query and update the radio state of Mobile Broadband devices.helpviewer_keywords: ["IMbnRadio","IMbnRadio interface [Microsoft Broadband Networks]","IMbnRadio interface [Microsoft Broadband Networks]","described","mbn.imbnradio","mbnapi/IMbnRadio"]
old-location: mbn\imbnradio.htm
tech.root: mbn
ms.assetid: b4b5ccfc-6cbf-4090-aee1-ee97092147f7
ms.date: 12/05/2018
ms.keywords: IMbnRadio, IMbnRadio interface [Microsoft Broadband Networks], IMbnRadio interface [Microsoft Broadband Networks],described, mbn.imbnradio, mbnapi/IMbnRadio
f1_keywords:
- mbnapi/IMbnRadio
dev_langs:
- c++
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
- IMbnRadio
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnRadio interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>IMbnRadio</b> interface is used to query and update the radio state of Mobile Broadband devices.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnRadio</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnRadio</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IMbnRadio</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnradio-setsoftwareradiostate">SetSoftwareRadioState</a>
</td>
<td align="left" width="63%">
Sets the software radio state.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnRadio</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnradio-get_hardwareradiostate">HardwareRadioState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The hardware radio state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnradio-get_softwareradiostate">SoftwareRadioState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The software radio state.

</td>
</tr>
</table> 


## -remarks



An application can acquire this interface by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method of <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>.




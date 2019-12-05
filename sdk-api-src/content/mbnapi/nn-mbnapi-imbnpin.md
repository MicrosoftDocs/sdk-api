---
UID: NN:mbnapi.IMbnPin
title: IMbnPin (mbnapi.h)
description: Represents the device PIN.
old-location: mbn\imbnpin.htm
tech.root: mbn
ms.assetid: 76764dbb-7de0-4b95-a210-60b8e6a4b24b
ms.date: 12/05/2018
ms.keywords: IMbnPin, IMbnPin interface [Microsoft Broadband Networks], IMbnPin interface [Microsoft Broadband Networks],described, mbn.imbnpin, mbnapi/IMbnPin
ms.topic: interface
f1_keywords:
- mbnapi/IMbnPin
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
- IMbnPin
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnPin interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Represents the device PIN.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnPin</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnPin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IMbnPin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-change">Change</a>
</td>
<td align="left" width="63%">
Changes the PIN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-disable">Disable</a>
</td>
<td align="left" width="63%">
Disables a PIN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-enable">Enable</a>
</td>
<td align="left" width="63%">
Enables a PIN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-enter">Enter</a>
</td>
<td align="left" width="63%">
Enters a PIN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-getpinmanager">GetPinManager</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock">Unblock</a>
</td>
<td align="left" width="63%">
Unblocks a blocked PIN.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnPin</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-get_pinformat">PinFormat</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The PIN format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-get_pinlengthmax">PinLengthMax</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The maximum length of the PIN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-get_pinlengthmin">PinLengthMin</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The minimum length of the PIN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-get_pinmode">PinMode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The PIN mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-get_pintype">PinType</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
    The PIN type.

</td>
</tr>
</table> 


## -remarks



<b>IMbnPin</b> objects are provided by calls to the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanager-getpin">GetPin</a> and <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanager-getpinlist">GetPinList</a> methods of the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a> interface.




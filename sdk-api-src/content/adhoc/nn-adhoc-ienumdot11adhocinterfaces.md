---
UID: NN:adhoc.IEnumDot11AdHocInterfaces
title: IEnumDot11AdHocInterfaces (adhoc.h)
description: Represents the collection of currently visible 802.11 ad hoc network interfaces.
old-location: nwifi\ienumdot11adhocinterfaces.htm
tech.root: NativeWiFi
ms.assetid: c61bbe3a-ad02-4182-bf10-1ed5fe307bd4
ms.date: 12/05/2018
ms.keywords: IEnumDot11AdHocInterfaces, IEnumDot11AdHocInterfaces interface [NativeWIFI], IEnumDot11AdHocInterfaces interface [NativeWIFI],described, adhoc/IEnumDot11AdHocInterfaces, nwifi.ienumdot11adhocinterfaces
ms.topic: interface
f1_keywords:
- adhoc/IEnumDot11AdHocInterfaces
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
- IEnumDot11AdHocInterfaces
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumDot11AdHocInterfaces interface


## -description


This interface represents the collection of currently visible 802.11 ad hoc network interfaces. It is a standard enumerator.
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="https://docs.microsoft.com/windows/desktop/NativeWiFi/about-the-wi-fi-direct-api">Wi-Fi Direct</a> instead.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumDot11AdHocInterfaces</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumDot11AdHocInterfaces</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumDot11AdHocInterfaces</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-ienumdot11adhocinterfaces-clone">IEnumDot11AdHocInterfaces::Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumeration interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-ienumdot11adhocinterfaces-next">IEnumDot11AdHocInterfaces::Next</a>
</td>
<td align="left" width="63%">
Gets the specified number of elements from the sequence and advances the current position by the number of items retrieved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-ienumdot11adhocinterfaces-reset">IEnumDot11AdHocInterfaces::Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/adhoc/nf-adhoc-ienumdot11adhocinterfaces-skip">IEnumDot11AdHocInterfaces::Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


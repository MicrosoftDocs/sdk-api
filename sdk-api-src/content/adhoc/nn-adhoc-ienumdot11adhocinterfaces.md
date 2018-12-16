---
UID: NN:adhoc.IEnumDot11AdHocInterfaces
title: IEnumDot11AdHocInterfaces
author: windows-sdk-content
description: Represents the collection of currently visible 802.11 ad hoc network interfaces.
old-location: nwifi\ienumdot11adhocinterfaces.htm
tech.root: NativeWiFi
ms.assetid: c61bbe3a-ad02-4182-bf10-1ed5fe307bd4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumDot11AdHocInterfaces, IEnumDot11AdHocInterfaces interface [NativeWIFI], IEnumDot11AdHocInterfaces interface [NativeWIFI],described, adhoc/IEnumDot11AdHocInterfaces, nwifi.ienumdot11adhocinterfaces
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumDot11AdHocInterfaces interface


## -description


This interface represents the collection of currently visible 802.11 ad hoc network interfaces. It is a standard enumerator.
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="https://msdn.microsoft.com/A649EBBA-1076-4426-9C4D-85AB8C415C66">Wi-Fi Direct</a> instead.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumDot11AdHocInterfaces</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumDot11AdHocInterfaces</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3169ff1e-1994-4dd9-920d-c3f270f17b1c">IEnumDot11AdHocInterfaces::Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumeration interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c20e215-a4ef-456e-ba19-0d9268279bf3">IEnumDot11AdHocInterfaces::Next</a>
</td>
<td align="left" width="63%">
Gets the specified number of elements from the sequence and advances the current position by the number of items retrieved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e310cc06-acc0-4a65-bea7-c9b39900b7ca">IEnumDot11AdHocInterfaces::Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5c61005-3de0-420e-a1ff-2c5f08bcc67f">IEnumDot11AdHocInterfaces::Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


---
UID: NN:adhoc.IEnumDot11AdHocNetworks
title: IEnumDot11AdHocNetworks
author: windows-sdk-content
description: Represents the collection of currently visible 802.11 ad hoc networks.
old-location: nwifi\ienumdot11adhocnetworks.htm
tech.root: NativeWiFi
ms.assetid: 5818e921-86bc-4f96-9ecd-3cb9c9a1a488
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumDot11AdHocNetworks, IEnumDot11AdHocNetworks interface [NativeWIFI], IEnumDot11AdHocNetworks interface [NativeWIFI],described, adhoc/IEnumDot11AdHocNetworks, nwifi.ienumdot11adhocnetworks
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
 - IEnumDot11AdHocNetworks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumDot11AdHocNetworks interface


## -description


This interface represents the collection of currently visible 802.11 ad hoc networks. It is a standard enumerator.
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="https://msdn.microsoft.com/A649EBBA-1076-4426-9C4D-85AB8C415C66">Wi-Fi Direct</a> instead.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumDot11AdHocNetworks</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumDot11AdHocNetworks</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumDot11AdHocNetworks</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/595829c6-ca87-4a69-8d09-a398b5cd9f34">IEnumDot11AdHocNetworks::Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumeration interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a695c8dd-5bde-41ff-8214-046e0a8cc26f">IEnumDot11AdHocNetworks::Next</a>
</td>
<td align="left" width="63%">
Gets the specified number of elements from the sequence and advances the current position by the number of items retrieved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8859b8e-9d77-423e-897c-a2c8cdea38ae">IEnumDot11AdHocNetworks::Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31e182f8-6a19-4138-b799-7ad485868d19">IEnumDot11AdHocNetworks::Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


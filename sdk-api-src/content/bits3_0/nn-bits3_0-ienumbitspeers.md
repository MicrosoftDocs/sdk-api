---
UID: NN:bits3_0.IEnumBitsPeers
title: IEnumBitsPeers
author: windows-sdk-content
description: Use IEnumBitsPeers to enumerate the list of peers that BITS has discovered.
old-location: bits\ienumbitspeers.htm
tech.root: bits
ms.assetid: 2715a58c-ba76-4223-ad9e-453d029e0eda
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumBitsPeers, IEnumBitsPeers interface [BITS], IEnumBitsPeers interface [BITS],described, bits.ienumbitspeers, bits3_0/IEnumBitsPeers
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IEnumBitsPeers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumBitsPeers interface


## -description


Use <b>IEnumBitsPeers</b> to enumerate the list of peers that BITS has discovered. 

To get this interface, call the 
<a href="https://msdn.microsoft.com/en-us/library/Aa964278(v=VS.85).aspx">IBitsPeerCacheAdministration::EnumPeers</a> method.
<div class="alert"><b>Note</b>  This interface is deprecated in BITS 4.0, and all of the API methods will return <b>S_FALSE</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumBitsPeers</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IEnumBitsPeers</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IEnumBitsPeers</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964309(v=VS.85).aspx">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964310(v=VS.85).aspx">GetCount</a>
</td>
<td align="left" width="63%">
Returns the number of items in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964311(v=VS.85).aspx">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964312(v=VS.85).aspx">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964313(v=VS.85).aspx">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of items in the enumeration sequence.

</td>
</tr>
</table> 


---
UID: NN:bits3_0.IEnumBitsPeers
title: IEnumBitsPeers
author: windows-sdk-content
description: Use IEnumBitsPeers to enumerate the list of peers that BITS has discovered.
old-location: bits\ienumbitspeers.htm
tech.root: Bits
ms.assetid: 2715a58c-ba76-4223-ad9e-453d029e0eda
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IEnumBitsPeers, IEnumBitsPeers interface [BITS], IEnumBitsPeers interface [BITS],described, bits.ienumbitspeers, bits3_0/IEnumBitsPeers
ms.prod: windows
ms.technology: windows-sdk
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
<a href="https://msdn.microsoft.com/8786d7d8-9ffb-4492-9834-90b97f97e4cf">IBitsPeerCacheAdministration::EnumPeers</a> method.
<div class="alert"><b>Note</b>  This interface is deprecated in BITS 4.0, and all of the API methods will return <b>S_FALSE</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumBitsPeers</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumBitsPeers</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/72b3e0bc-9426-4953-a910-2dfaa955c4c0">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4e52429-cd41-483a-b168-b5d7a1f77d74">GetCount</a>
</td>
<td align="left" width="63%">
Returns the number of items in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5bc254d-d74e-4076-a22a-93abf9023068">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87eb8e34-046e-46a5-9d9b-efeb6fa03485">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23a9b424-11a3-4cbf-a867-93026f0725cc">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of items in the enumeration sequence.

</td>
</tr>
</table> 


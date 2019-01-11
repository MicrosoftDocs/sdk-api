---
UID: NN:bits3_0.IEnumBitsPeerCacheRecords
title: IEnumBitsPeerCacheRecords
author: windows-sdk-content
description: Use IEnumBitsPeerCacheRecords to enumerate the records of the cache.
old-location: bits\ienumbitspeercacherecords.htm
tech.root: Bits
ms.assetid: 680c1468-d780-44a3-9048-c7c3928234f9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumBitsPeerCacheRecords, IEnumBitsPeerCacheRecords interface [BITS], IEnumBitsPeerCacheRecords interface [BITS],described, bits.ienumbitspeercacherecords, bits3_0/IEnumBitsPeerCacheRecords
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
 - IEnumBitsPeerCacheRecords
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumBitsPeerCacheRecords interface


## -description


Use <b>IEnumBitsPeerCacheRecords</b> to enumerate the records of the cache. 

To get this interface, call the 
<a href="https://msdn.microsoft.com/b471cee0-0ad0-4488-9819-e524e50dbc76">IBitsPeerCacheAdministration::EnumRecords</a> method.
<div class="alert"><b>Note</b>  This interface is deprecated in BITS 4.0, and all of the API methods will return <b>S_FALSE</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumBitsPeerCacheRecords</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumBitsPeerCacheRecords</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumBitsPeerCacheRecords</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4eb19401-119d-4ce6-92b1-aa41b6dcb97c">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40c4e7da-031f-4c3b-ab18-2476b54ae972">GetCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8117baa-9f77-4735-bd15-2c7e1e759e9b">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1e1dbdc-a90d-4ac8-8b52-8e4f914a81dd">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1204e4b-985e-4d3e-8a1f-d13d46e8f1ce">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of items in the enumeration sequence.

</td>
</tr>
</table> 


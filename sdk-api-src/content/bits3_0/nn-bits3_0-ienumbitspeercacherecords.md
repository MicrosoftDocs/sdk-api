---
UID: NN:bits3_0.IEnumBitsPeerCacheRecords
title: IEnumBitsPeerCacheRecords (bits3_0.h)
author: windows-sdk-content
description: Use IEnumBitsPeerCacheRecords to enumerate the records of the cache.
old-location: bits\ienumbitspeercacherecords.htm
tech.root: Bits
ms.assetid: 680c1468-d780-44a3-9048-c7c3928234f9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumBitsPeerCacheRecords, IEnumBitsPeerCacheRecords interface [BITS], IEnumBitsPeerCacheRecords interface [BITS],described, bits.ienumbitspeercacherecords, bits3_0/IEnumBitsPeerCacheRecords
ms.topic: interface
f1_keywords: 
 - "bits3_0/IEnumBitsPeerCacheRecords"
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
ms.custom: 19H1
---

# IEnumBitsPeerCacheRecords interface


## -description


Use <b>IEnumBitsPeerCacheRecords</b> to enumerate the records of the cache. 

To get this interface, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nf-bits3_0-ibitspeercacheadministration-enumrecords">IBitsPeerCacheAdministration::EnumRecords</a> method.
<div class="alert"><b>Note</b>  This interface is deprecated in BITS 4.0, and all of the API methods will return <b>S_FALSE</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumBitsPeerCacheRecords</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumBitsPeerCacheRecords</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nf-bits3_0-ienumbitspeercacherecords-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nf-bits3_0-ienumbitspeercacherecords-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of items in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nf-bits3_0-ienumbitspeercacherecords-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nf-bits3_0-ienumbitspeercacherecords-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bits3_0/nf-bits3_0-ienumbitspeercacherecords-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of items in the enumeration sequence.

</td>
</tr>
</table> 


---
UID: NN:mpeg2data.ISectionList
title: ISectionList
author: windows-driver-content
description: The ISectionList interface represents a list of MPEG-2 table sections.
old-location: mstv\isectionlist.htm
old-project: mstv
ms.assetid: eb6d31b4-ee4a-468f-9e58-115159095858
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ISectionList, ISectionList interface [Microsoft TV Technologies], ISectionList interface [Microsoft TV Technologies], described, ISectionListInterface, mpeg2data/ISectionList, mstv.isectionlist
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mpeg2data.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mpeg2data.h
api_name:
-	ISectionList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ISectionList interface


## -description



The <b>ISectionList</b> interface represents a list of MPEG-2 table sections.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISectionList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISectionList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISectionList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58e0898d-a84e-49cf-bc18-1fda8351dfc0">CancelPendingRequest</a>
</td>
<td align="left" width="63%">
Cancels any pending asynchronous request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b9e3383-7b84-4c4e-87cf-8e3a37d3b81b">GetNumberOfSections</a>
</td>
<td align="left" width="63%">
Returns the number of MPEG-2 sections that were received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25a4bd3c-ef02-4685-8c83-06025ce4410c">GetProgramIdentifier</a>
</td>
<td align="left" width="63%">
Retrieves the program identifier (PID) of the packets that this object is receiving.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b03d1727-9ebd-4e78-b7d0-c6d0959aab8a">GetSectionData</a>
</td>
<td align="left" width="63%">
Retrieves a section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0fd82ec-283e-4d6f-aa74-c65f15df651f">GetTableIdentifier</a>
</td>
<td align="left" width="63%">
Returns the table identifier (TID) of the packets that this object is receiving.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61f1e99b-c375-4aa3-a11b-7e24c35f71ca">InitializeWithRawSections</a>
</td>
<td align="left" width="63%">
Initializes the object with raw section data.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ISectionList)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 


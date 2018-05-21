---
UID: NN:strmif.IEnumFilters
title: IEnumFilters
author: windows-driver-content
description: The IEnumFilters interface enumerates the filters in a filter graph.
old-location: dshow\ienumfilters.htm
old-project: DirectShow
ms.assetid: e105ccff-86c6-45d5-aead-6d303d038e5a
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IEnumFilters, IEnumFilters interface [DirectShow], IEnumFilters interface [DirectShow],described, IEnumFiltersInterface, dshow.ienumfilters, strmif/IEnumFilters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IEnumFilters
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IEnumFilters interface


## -description



The <code>IEnumFilters</code> interface enumerates the filters in a filter graph. To obtain this interface, call the <a href="https://msdn.microsoft.com/3a6dcd1a-3ec3-4f0f-8e82-2d33ad775eec">IFilterGraph::EnumFilters</a> method on the Filter Graph Manager. For more information, see <a href="https://msdn.microsoft.com/04a3dbc8-33c4-4b70-930e-686be2f8301f">Enumerating Objects in a Filter Graph</a>.

This interface implements a standard Component Object Model (COM) collection object.

If the set of filters in the graph changes, some methods on this interface return VFW_E_ENUM_OUT_OF_SYNC. Call the <a href="https://msdn.microsoft.com/997a6e56-cd11-42bf-b12c-a4418a4dc644">IEnumFilters::Reset</a> method to resynchronize the enumerator.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumFilters</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumFilters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumFilters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Makes a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of filters in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skips over a specified number of filters.

</td>
</tr>
</table> 


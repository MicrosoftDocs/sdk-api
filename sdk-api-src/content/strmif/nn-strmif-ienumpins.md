---
UID: NN:strmif.IEnumPins
title: IEnumPins
author: windows-sdk-content
description: Enumerates pins on a filter.The IBaseFilter::EnumPins method returns this interface.
old-location: dshow\ienumpins.htm
tech.root: DirectShow
ms.assetid: 839190b4-fd29-4a94-8838-d84adfdd9668
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IEnumPins, IEnumPins interface [DirectShow], IEnumPins interface [DirectShow],described, IEnumPinsInterface, dshow.ienumpins, strmif/IEnumPins
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IEnumPins
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumPins interface


## -description



Enumerates pins on a filter.

The <a href="https://msdn.microsoft.com/02675c93-7901-40f6-a9fc-f6f13f56acca">IBaseFilter::EnumPins</a> method returns this interface. It is based on the standard Component Object Model (COM) enumerators. 

The filter graph manager uses this interface when it connects filters. Applications can use it to retrieve pins on a filter. For more information, see <a href="https://msdn.microsoft.com/04a3dbc8-33c4-4b70-930e-686be2f8301f">Enumerating Objects in a Filter Graph</a>.

If the number of pins on the filter changes, some methods on this interface return VFW_E_ENUM_OUT_OF_SYNC. Call the <a href="https://msdn.microsoft.com/c2147884-aec2-43ae-b85a-61383ad6ca15">IEnumPins::Reset</a> method to resynchronize the enumerator.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumPins</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumPins</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumPins</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/946bb08e-6866-46b3-b2d7-de2ab6c5e608">Clone</a>
</td>
<td align="left" width="63%">
Makes a copy of the enumerator with the same enumeration state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03a30eb6-b39f-4497-ad3f-8af2c3ecf2f0">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of pins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2147884-aec2-43ae-b85a-61383ad6ca15">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/501d08ee-ebd1-48dc-8cc9-bf017034b4cd">Skip</a>
</td>
<td align="left" width="63%">
Skips over a specified number of pins.

</td>
</tr>
</table> 


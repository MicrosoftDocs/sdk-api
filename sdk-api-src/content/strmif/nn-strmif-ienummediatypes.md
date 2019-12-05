---
UID: NN:strmif.IEnumMediaTypes
title: IEnumMediaTypes (strmif.h)
description: The IEnumMediaTypes interface enumerates a pin's preferred media types.
old-location: dshow\ienummediatypes.htm
tech.root: DirectShow
ms.assetid: e0021e27-0e08-4d07-9610-08a9b945ae34
ms.date: 12/05/2018
ms.keywords: IEnumMediaTypes, IEnumMediaTypes interface [DirectShow], IEnumMediaTypes interface [DirectShow],described, IEnumMediaTypesInterface, dshow.ienummediatypes, strmif/IEnumMediaTypes
ms.topic: interface
f1_keywords:
- strmif/IEnumMediaTypes
dev_langs:
- c++
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
- IEnumMediaTypes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumMediaTypes interface


## -description


The <b>IEnumMediaTypes</b> interface enumerates a pin's preferred media types. To obtain this interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipin-enummediatypes">IPin::EnumMediaTypes</a> method on the pin. Filters use this interface when they connect to other filters. Applications can also use it to examine a pin's preferred media types. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/enumerating-objects-in-a-filter-graph">Enumerating Objects in a Filter Graph</a>.

This interface implements a standard Component Object Model (COM) collection object. 

If a pin's set of preferred media types changes, some methods on this interface return <b>VFW_E_ENUM_OUT_OF_SYNC</b>. Call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienummediatypes-reset">IEnumMediaTypes::Reset</a> method to resynchronize the enumerator.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumMediaTypes</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumMediaTypes</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumMediaTypes</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienummediatypes-clone">Clone</a>
</td>
<td align="left" width="63%">
Makes a copy of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienummediatypes-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of media types.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienummediatypes-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienummediatypes-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over a specified number of media types.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/enumerating-media-types">Enumerating Media Types</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 


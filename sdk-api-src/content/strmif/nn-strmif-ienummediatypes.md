---
UID: NN:strmif.IEnumMediaTypes
title: IEnumMediaTypes (strmif.h)
description: The IEnumMediaTypes interface enumerates a pin's preferred media types.
helpviewer_keywords: ["IEnumMediaTypes","IEnumMediaTypes interface [DirectShow]","IEnumMediaTypes interface [DirectShow]","described","IEnumMediaTypesInterface","dshow.ienummediatypes","strmif/IEnumMediaTypes"]
old-location: dshow\ienummediatypes.htm
tech.root: dshow
ms.assetid: e0021e27-0e08-4d07-9610-08a9b945ae34
ms.date: 12/05/2018
ms.keywords: IEnumMediaTypes, IEnumMediaTypes interface [DirectShow], IEnumMediaTypes interface [DirectShow],described, IEnumMediaTypesInterface, dshow.ienummediatypes, strmif/IEnumMediaTypes
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumMediaTypes
 - strmif/IEnumMediaTypes
dev_langs:
 - c++
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
---

# IEnumMediaTypes interface


## -description

The <b>IEnumMediaTypes</b> interface enumerates a pin's preferred media types. To obtain this interface, call the <a href="/windows/desktop/api/strmif/nf-strmif-ipin-enummediatypes">IPin::EnumMediaTypes</a> method on the pin. Filters use this interface when they connect to other filters. Applications can also use it to examine a pin's preferred media types. For more information, see <a href="/windows/desktop/DirectShow/enumerating-objects-in-a-filter-graph">Enumerating Objects in a Filter Graph</a>.

This interface implements a standard Component Object Model (COM) collection object. 

If a pin's set of preferred media types changes, some methods on this interface return <b>VFW_E_ENUM_OUT_OF_SYNC</b>. Call the <a href="/windows/desktop/api/strmif/nf-strmif-ienummediatypes-reset">IEnumMediaTypes::Reset</a> method to resynchronize the enumerator.

## -inheritance

The <b>IEnumMediaTypes</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumMediaTypes</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/enumerating-media-types">Enumerating Media Types</a>



<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>

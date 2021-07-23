---
UID: NN:strmif.IEnumPins
title: IEnumPins (strmif.h)
description: Enumerates pins on a filter.The IBaseFilter::EnumPins method returns this interface.
helpviewer_keywords: ["IEnumPins","IEnumPins interface [DirectShow]","IEnumPins interface [DirectShow]","described","IEnumPinsInterface","dshow.ienumpins","strmif/IEnumPins"]
old-location: dshow\ienumpins.htm
tech.root: dshow
ms.assetid: 839190b4-fd29-4a94-8838-d84adfdd9668
ms.date: 12/05/2018
ms.keywords: IEnumPins, IEnumPins interface [DirectShow], IEnumPins interface [DirectShow],described, IEnumPinsInterface, dshow.ienumpins, strmif/IEnumPins
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
 - IEnumPins
 - strmif/IEnumPins
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
 - IEnumPins
---

# IEnumPins interface


## -description

Enumerates pins on a filter.

The <a href="/windows/desktop/api/strmif/nf-strmif-ibasefilter-enumpins">IBaseFilter::EnumPins</a> method returns this interface. It is based on the standard Component Object Model (COM) enumerators. 

The filter graph manager uses this interface when it connects filters. Applications can use it to retrieve pins on a filter. For more information, see <a href="/windows/desktop/DirectShow/enumerating-objects-in-a-filter-graph">Enumerating Objects in a Filter Graph</a>.

If the number of pins on the filter changes, some methods on this interface return VFW_E_ENUM_OUT_OF_SYNC. Call the <a href="/windows/desktop/api/strmif/nf-strmif-ienumpins-reset">IEnumPins::Reset</a> method to resynchronize the enumerator.

## -inheritance

The <b>IEnumPins</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumPins</b> also has these types of members:


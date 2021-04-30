---
UID: NS:strmif._PinInfo
title: PIN_INFO (strmif.h)
description: The PIN_INFO structure contains information about a pin.
helpviewer_keywords: ["PIN_INFO","PIN_INFO structure [DirectShow]","PIN_INFOStructure","dshow.pin_info","strmif/PIN_INFO"]
old-location: dshow\pin_info.htm
tech.root: dshow
ms.assetid: 67a837f3-8b81-4651-a0fa-fed7b61e71c2
ms.date: 12/05/2018
ms.keywords: PIN_INFO, PIN_INFO structure [DirectShow], PIN_INFOStructure, dshow.pin_info, strmif/PIN_INFO
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PIN_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PinInfo
 - strmif/_PinInfo
 - PIN_INFO
 - strmif/PIN_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - PIN_INFO
---

# PIN_INFO structure


## -description

The <code>PIN_INFO</code> structure contains information about a pin.

## -struct-fields

### -field pFilter

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of the owning filter.

### -field dir

Direction of the pin (input or output).

### -field achName

Name of the pin.

## -remarks

If the name of an output pin begins with a tilde (~), the filter graph manager ignores the pin when it builds a graph. During a call to <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-connect">IGraphBuilder::Connect</a>, <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-render">IGraphBuilder::Render</a>, or <a href="/windows/desktop/api/strmif/nf-strmif-igraphbuilder-renderfile">IGraphBuilder::RenderFile</a>, if the pin appears on an intermediate filter, the filter graph manager does not render the pin. However, it renders the pin if you explicitly pass the pin to the <b>Connect</b> or <b>Render</b> method.

Use a tilde if the pin delivers a secondary stream that should not be rendered by default, or if the pin requires special code to render correctly. For example, DVD filters should use it for pins that deliver subpicture or closed captioning data. Video capture filters should use it for capture pins (but not preview pins).

The <b>pFilter</b> member has an outstanding reference count. The application must release the interface.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ipin-querypininfo">IPin::QueryPinInfo</a>
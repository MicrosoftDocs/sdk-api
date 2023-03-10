---
UID: NF:windows.graphics.effects.interop.IGraphicsEffectD2D1Interop.GetNamedPropertyMapping
title: IGraphicsEffectD2D1Interop::GetNamedPropertyMapping (windows.graphics.effects.interop.h)
description: Retrieves the mapping for an effect property.
helpviewer_keywords: ["GetNamedPropertyMapping","GetNamedPropertyMapping method","GetNamedPropertyMapping method","IGraphicsEffectD2D1Interop interface","IGraphicsEffectD2D1Interop interface","GetNamedPropertyMapping method","IGraphicsEffectD2D1Interop.GetNamedPropertyMapping","IGraphicsEffectD2D1Interop.effects","IGraphicsEffectD2D1Interop::GetNamedPropertyMapping","IGraphicsEffectD2D1Interop::effects","w_graph_fx.igraphicseffectd2d1interop_getnamedpropertymapping","windows/IGraphicsEffectD2D1Interop::GetNamedPropertyMapping"]
old-location: w_graph_fx\igraphicseffectd2d1interop_getnamedpropertymapping.htm
tech.root: winrt
ms.assetid: 72185CB5-6D8A-4F9F-B913-C9216CECEC90
ms.date: 12/05/2018
ms.keywords: GetNamedPropertyMapping, GetNamedPropertyMapping method, GetNamedPropertyMapping method,IGraphicsEffectD2D1Interop interface, IGraphicsEffectD2D1Interop interface,GetNamedPropertyMapping method, IGraphicsEffectD2D1Interop.GetNamedPropertyMapping, IGraphicsEffectD2D1Interop.effects, IGraphicsEffectD2D1Interop::GetNamedPropertyMapping, IGraphicsEffectD2D1Interop::effects, w_graph_fx.igraphicseffectd2d1interop_getnamedpropertymapping, windows/IGraphicsEffectD2D1Interop::GetNamedPropertyMapping
req.header: windows.graphics.effects.interop.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGraphicsEffectD2D1Interop::GetNamedPropertyMapping
 - windows.graphics.effects.interop/IGraphicsEffectD2D1Interop::GetNamedPropertyMapping
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.graphics.effects.interop.h
api_name:
 - IGraphicsEffectD2D1Interop.GetNamedPropertyMapping
---

# IGraphicsEffectD2D1Interop::GetNamedPropertyMapping (windows.graphics.effects.interop.h)


## -description

Retrieves the mapping for an effect property.

## -parameters

### -param name

Type: <b>LPCWSTR</b>

Name of the property.

### -param index [out]

Type: <b>UINT*</b>

When this method returns, this parameter will contain the index of the property.

### -param mapping [out]

Type: <b><a href="/windows/desktop/api/windows.graphics.effects.interop/ne-windows-graphics-effects-interop-graphics_effect_property_mapping">GRAPHICS_EFFECT_PROPERTY_MAPPING</a>*</b>

Indicates how a strongly-typed effect property maps to an underlying Direct2D effect property.

## -returns

Type: <b>HRESULT</b>

This method returns an HRESULT success or error code.

## -see-also

<a href="/windows/desktop/api/windows.graphics.effects.interop/nn-windows-graphics-effects-interop-igraphicseffectd2d1interop">IGraphicsEffectD2D1Interop</a>

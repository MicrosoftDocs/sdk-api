---
UID: NC:d2d1effectauthor.PD2D1_PROPERTY_SET_FUNCTION
title: PD2D1_PROPERTY_SET_FUNCTION (d2d1effectauthor.h)
description: Sets a property on an effect.
helpviewer_keywords: ["PD2D1_PROPERTY_SET_FUNCTION","PD2D1_PROPERTY_SET_FUNCTION function","PD2D1_PROPERTY_SET_FUNCTION function pointer [Direct2D]","d2d1effectauthor/PD2D1_PROPERTY_SET_FUNCTION","direct2d.pd2d1_property_set_function"]
old-location: direct2d\pd2d1_property_set_function.htm
tech.root: Direct2D
ms.assetid: 3293F53E-B911-4F5F-9510-E91B5261BB90
ms.date: 12/05/2018
ms.keywords: PD2D1_PROPERTY_SET_FUNCTION, PD2D1_PROPERTY_SET_FUNCTION function, PD2D1_PROPERTY_SET_FUNCTION function pointer [Direct2D], d2d1effectauthor/PD2D1_PROPERTY_SET_FUNCTION, direct2d.pd2d1_property_set_function
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - PD2D1_PROPERTY_SET_FUNCTION
 - d2d1effectauthor/PD2D1_PROPERTY_SET_FUNCTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - D2d1effectauthor.h
api_name:
 - PD2D1_PROPERTY_SET_FUNCTION
---

# PD2D1_PROPERTY_SET_FUNCTION callback function


## -description

Sets a property on an effect.

## -parameters

### -param effect [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface for the effect on which the property will be set.

### -param data [in]

A pointer to the data to be set on the property.

### -param dataSize

The number of bytes in the property set by the function.

## -returns

Returns S_OK if successful; otherwise, returns an <b>HRESULT</b> error code.

## -remarks

Supply a <b>PD2D1_PROPERTY_SET_FUNCTION</b> function pointer to the <b>setFunction</b> member of a <a href="/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding">D2D1_PROPERTY_BINDING</a> structure to specify the function that Direct2D uses to set data for a property.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding">D2D1_PROPERTY_BINDING</a>

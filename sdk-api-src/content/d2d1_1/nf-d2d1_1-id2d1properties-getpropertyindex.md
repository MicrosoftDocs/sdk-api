---
UID: NF:d2d1_1.ID2D1Properties.GetPropertyIndex
title: ID2D1Properties::GetPropertyIndex
description: Gets the index corresponding to the given property name.
helpviewer_keywords: ["GetPropertyIndex","GetPropertyIndex method [Direct2D]","GetPropertyIndex method [Direct2D]","ID2D1Properties interface","ID2D1Properties interface [Direct2D]","GetPropertyIndex method","ID2D1Properties.GetPropertyIndex","ID2D1Properties::GetPropertyIndex","d2d1_1/ID2D1Properties::GetPropertyIndex","direct2d.id2d1properties_getpropertyindex"]
old-location: direct2d\id2d1properties_getpropertyindex.htm
tech.root: Direct2D
ms.assetid: b1c7003f-b7c2-464c-8e8e-a641068b9393
ms.date: 09/19/2019
ms.keywords: GetPropertyIndex, GetPropertyIndex method [Direct2D], GetPropertyIndex method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetPropertyIndex method, ID2D1Properties.GetPropertyIndex, ID2D1Properties::GetPropertyIndex, d2d1_1/ID2D1Properties::GetPropertyIndex, direct2d.id2d1properties_getpropertyindex
req.header: d2d1_1.h
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - ID2D1Properties::GetPropertyIndex
 - d2d1_1/ID2D1Properties::GetPropertyIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Properties.GetPropertyIndex
---

## -description

Gets the index corresponding to the given property name.

## -parameters

### -param name [in]

Type: <b>PCWSTR</b>

The name of the property to retrieve.

## -returns

Type: <b>UINT32</b>

The index of the corresponding property name.

## -remarks

If the property doesn't exist, then this method returns [D2D1_INVALID_PROPERTY_INDEX](/windows/win32/direct2d/direct2d-constants#d2d1_invalid_property_index-uintmax). This reserved value will never map to a valid index, and will cause <b>NULL</b> or sentinel values to be returned from other parts of the property interface.

## -see-also

[D2D1_INVALID_PROPERTY_INDEX](/windows/win32/direct2d/direct2d-constants#d2d1_invalid_property_index-uintmax)

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a>
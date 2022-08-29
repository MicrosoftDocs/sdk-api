---
UID: NS:d2d1_1helper.TypeTraits
title: TypeTraits (d2d1_1helper.h)
description: The TypeTraits (d2d1_1helper.h) structure contains implementations of Point, Size, and Rect that store their data using the specified type.
helpviewer_keywords: ["TypeTraits","TypeTraits structure [Direct2D]","TypeTraits<Type>","d2d1helper/TypeTraits","direct2d.typetraits_t_"]
old-location: direct2d\typetraits_t_.htm
tech.root: Direct2D
ms.assetid: 18003d9f-4202-4bea-9580-bbf8fcdbca8f
ms.date: 08/10/2022
ms.keywords: TypeTraits, TypeTraits structure [Direct2D], TypeTraits<Type>, d2d1helper/TypeTraits, direct2d.typetraits_t_
req.header: d2d1_1helper.h
req.include-header: D2d1_1helper.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - TypeTraits
 - d2d1_1helper/TypeTraits
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1helper.h
api_name:
 - TypeTraits
---

## -description

Contains implementations of <b>Point</b>, <b>Size</b>, and <b>Rect</b> that store their data using the specified type.

## -struct-fields

## -syntax

```cpp
template<typename Type>
struct TypeTraits
{
    typedef D2D1_POINT_2F Point;
    typedef D2D1_SIZE_F   Size;
    typedef D2D1_RECT_F   Rect;
};

template<>
struct TypeTraits<UINT32>
{
    typedef D2D1_POINT_2U Point;
    typedef D2D1_SIZE_U   Size;
    typedef D2D1_RECT_U   Rect;
};
```


---
UID: NF:d2d1_1.ID2D1Properties.GetType(U)
title: ID2D1Properties::GetType(U,) (d2d1_1.h)
description: Gets the D2D1_PROPERTY_TYPE of the selected property. This is a template overload. See Remarks.
helpviewer_keywords: ["GetType","GetType method [Direct2D]","GetType method [Direct2D]","ID2D1Properties interface","ID2D1Properties interface [Direct2D]","GetType method","ID2D1Properties.GetType","ID2D1Properties.GetType(U",")","ID2D1Properties::GetType","ID2D1Properties::GetType(U)","ID2D1Properties::GetType(U",")","d2d1_1/ID2D1Properties::GetType","direct2d.id2d1properties_gettype2"]
old-location: direct2d\id2d1properties_gettype2.htm
tech.root: Direct2D
ms.assetid: 4EFE306B-DE39-4536-8BE0-8036A380E2BD
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [Direct2D], GetType method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetType method, ID2D1Properties.GetType, ID2D1Properties.GetType(U,), ID2D1Properties::GetType, ID2D1Properties::GetType(U), ID2D1Properties::GetType(U,), d2d1_1/ID2D1Properties::GetType, direct2d.id2d1properties_gettype2
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Properties::GetType
 - d2d1_1/ID2D1Properties::GetType
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
 - ID2D1Properties.GetType
---

# ID2D1Properties::GetType(U)


## -description

Gets the <a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property_type">D2D1_PROPERTY_TYPE</a> of the selected property.

This is a template overload. See Remarks.

## -parameters

### -param index

Type: <b>U</b>

The index of the property for which the type will be retrieved.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property_type">D2D1_PROPERTY_TYPE</a></b>

This method returns a <a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property_type">D2D1_PROPERTY_TYPE</a>-typed value for the type of the selected property.

## -remarks

If the property does not exist, the method returns <a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property_type">D2D1_PROPERTY_TYPE_UNKNOWN</a>.


<pre class="syntax">template&lt;typename U&gt;
    D2D1_PROPERTY_TYPE GetType(
        U index
        ) CONST;
</pre>

## -see-also

<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property">D2D1_PROPERTY</a>



<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property_type">D2D1_PROPERTY_TYPE</a>



<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_subproperty">D2D1_SUBPROPERTY</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a>

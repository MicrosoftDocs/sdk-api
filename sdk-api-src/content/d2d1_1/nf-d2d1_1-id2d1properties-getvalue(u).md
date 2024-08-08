---
UID: NF:d2d1_1.ID2D1Properties.GetValue(U)
title: ID2D1Properties::GetValue(U,) (d2d1_1.h)
description: Gets the value of the property by index. This is a template overload. See Remarks. (overload 1/2)
helpviewer_keywords: ["GetValue","GetValue method [Direct2D]","GetValue method [Direct2D]","ID2D1Properties interface","ID2D1Properties interface [Direct2D]","GetValue method","ID2D1Properties.GetValue","ID2D1Properties.GetValue(U",")","ID2D1Properties::GetValue","ID2D1Properties::GetValue(U)","ID2D1Properties::GetValue(U",")","d2d1_1/ID2D1Properties::GetValue","direct2d.id2d1properties_getvalue5"]
old-location: direct2d\id2d1properties_getvalue5.htm
tech.root: Direct2D
ms.assetid: 90E54C63-B584-4844-85B7-BCCF766D90E3
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [Direct2D], GetValue method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetValue method, ID2D1Properties.GetValue, ID2D1Properties.GetValue(U,), ID2D1Properties::GetValue, ID2D1Properties::GetValue(U), ID2D1Properties::GetValue(U,), d2d1_1/ID2D1Properties::GetValue, direct2d.id2d1properties_getvalue5
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
 - ID2D1Properties::GetValue
 - d2d1_1/ID2D1Properties::GetValue
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
 - ID2D1Properties.GetValue
---

# ID2D1Properties::GetValue(U)


## -description

Gets  the value of the property by index. This is a template overload. See Remarks.

## -parameters

### -param index

Type: <b>U</b>

The index of the property from which the value is to be obtained.

## -returns

Type: <b>T</b>

Returns the value requested.

## -remarks

<pre class="syntax">template&lt;typename T, typename U&gt;
    T GetValue(
        U index
        ) const;
</pre>

## -see-also

<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property">D2D1_PROPERTY</a>



<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_subproperty">D2D1_SUBPROPERTY</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a>

---
UID: NF:d2d1_3.ID2D1DeviceContext2.CreateInkStyle(constD2D1_INK_STYLE_PROPERTIES&,ID2D1InkStyle)
title: ID2D1DeviceContext2::CreateInkStyle(const D2D1_INK_STYLE_PROPERTIES &,ID2D1InkStyle) (d2d1_3.h)
description: Creates a new ID2D1InkStyle object, for use with ink rendering methods such as DrawInk. (overload 1/2)
helpviewer_keywords: ["CreateInkStyle","CreateInkStyle method [Direct2D]","CreateInkStyle method [Direct2D]","ID2D1DeviceContext2 interface","ID2D1DeviceContext2 interface [Direct2D]","CreateInkStyle method","ID2D1DeviceContext2.CreateInkStyle","ID2D1DeviceContext2.CreateInkStyle(const D2D1_INK_STYLE_PROPERTIES &","ID2D1InkStyle)","ID2D1DeviceContext2::CreateInkStyle","ID2D1DeviceContext2::CreateInkStyle(const D2D1_INK_STYLE_PROPERTIES &","ID2D1InkStyle)","d2d1_3/ID2D1DeviceContext2::CreateInkStyle","direct2d.id2d1devicecontext2_createinkstyle"]
old-location: direct2d\id2d1devicecontext2_createinkstyle.htm
tech.root: Direct2D
ms.assetid: 6d219a50-da5f-b5ff-e819-70b2dc5f538c
ms.date: 12/05/2018
ms.keywords: CreateInkStyle, CreateInkStyle method [Direct2D], CreateInkStyle method [Direct2D],ID2D1DeviceContext2 interface, ID2D1DeviceContext2 interface [Direct2D],CreateInkStyle method, ID2D1DeviceContext2.CreateInkStyle, ID2D1DeviceContext2.CreateInkStyle(const D2D1_INK_STYLE_PROPERTIES &,ID2D1InkStyle), ID2D1DeviceContext2::CreateInkStyle, ID2D1DeviceContext2::CreateInkStyle(const D2D1_INK_STYLE_PROPERTIES &,ID2D1InkStyle), d2d1_3/ID2D1DeviceContext2::CreateInkStyle, direct2d.id2d1devicecontext2_createinkstyle
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext2::CreateInkStyle
 - d2d1_3/ID2D1DeviceContext2::CreateInkStyle
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
 - ID2D1DeviceContext2.CreateInkStyle
---

# ID2D1DeviceContext2::CreateInkStyle(const D2D1_INK_STYLE_PROPERTIES &,ID2D1InkStyle)


## -description

Creates a new <a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1inkstyle">ID2D1InkStyle</a> object, for use with ink 
        rendering methods such as <a href="/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawink">DrawInk</a>.

## -parameters

### -param inkStyleProperties [ref]

Type: <b>const <a href="/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_style_properties">D2D1_INK_STYLE_PROPERTIES</a></b>

The properties of the ink style to be created.

### -param inkStyle [out]

Type: <b><a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1inkstyle">ID2D1InkStyle</a>**</b>

When this method returns, contains the address of a pointer to a new ink style object.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

S_OK if successful, otherwise a failure HRESULT.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2">ID2D1DeviceContext2</a>

---
UID: NF:d2d1_1helper.SetDpiCompensatedEffectInput
title: SetDpiCompensatedEffectInput function (d2d1_1helper.h)
description: Sets a bitmap as an effect input, while inserting a DPI compensation effect to preserve visual appearance as the device context's DPI changes.
helpviewer_keywords: ["SetDpiCompensatedEffectInput","SetDpiCompensatedEffectInput function [Direct2D]","d2d1_1helper/SetDpiCompensatedEffectInput","direct2d.setdpicompensatedeffectinput"]
old-location: direct2d\setdpicompensatedeffectinput.htm
tech.root: Direct2D
ms.assetid: B9E2C5F7-2E05-441D-A902-6473E0235659
ms.date: 12/05/2018
ms.keywords: SetDpiCompensatedEffectInput, SetDpiCompensatedEffectInput function [Direct2D], d2d1_1helper/SetDpiCompensatedEffectInput, direct2d.setdpicompensatedeffectinput
req.header: d2d1_1helper.h
req.include-header: 
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetDpiCompensatedEffectInput
 - d2d1_1helper/SetDpiCompensatedEffectInput
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - SetDpiCompensatedEffectInput
---

# SetDpiCompensatedEffectInput function


## -description

Sets a bitmap as an effect input, while inserting a DPI compensation effect
    to preserve visual appearance as the device context's DPI changes.

## -parameters

### -param deviceContext [in]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>*</b>

The device context that is the creator of the effect.

### -param effect [in]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>*</b>

The function sets the input of this effect.

### -param inputIndex

Type: <b>UINT32</b>

The index of the input to be set.

### -param inputBitmap [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>*</b>

The input bitmap.

### -param interpolationMode

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode">D2D1_INTERPOLATION_MODE</a></b>

The interpolation mode for the DPI compensation effect.

### -param borderMode

Type: <b><a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_border_mode">D2D1_BORDER_MODE</a></b>

The border mode for the DPI compensation effect.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
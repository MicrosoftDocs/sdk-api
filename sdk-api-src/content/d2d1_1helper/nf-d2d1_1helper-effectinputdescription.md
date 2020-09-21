---
UID: NF:d2d1_1helper.EffectInputDescription
title: EffectInputDescription function (d2d1_1helper.h)
description: Creates a D2D1_EFFECT_INPUT_DESCRIPTION structure.
helpviewer_keywords: ["EffectInputDescription","EffectInputDescription function [Direct2D]","d2d1_1helper/EffectInputDescription","direct2d.effectinputdescription"]
old-location: direct2d\effectinputdescription.htm
tech.root: Direct2D
ms.assetid: 3246476C-4110-43EC-88A3-55682A141383
ms.date: 12/05/2018
ms.keywords: EffectInputDescription, EffectInputDescription function [Direct2D], d2d1_1helper/EffectInputDescription, direct2d.effectinputdescription
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
 - EffectInputDescription
 - d2d1_1helper/EffectInputDescription
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
 - EffectInputDescription
---

# EffectInputDescription function


## -description

Creates a <a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_effect_input_description">D2D1_EFFECT_INPUT_DESCRIPTION</a> structure.

## -parameters

### -param effect

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a>*</b>

The effect whose input connection is being specified.

### -param inputIndex

Type: <b>UINT32</b>

The input index of the effect that is being considered.

### -param inputRectangle

Type: <b><a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a></b>

The amount of data that would be available on the input. This can be used to query this information when the data is not yet available.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_effect_input_description">D2D1_EFFECT_INPUT_DESCRIPTION</a></b>

The filled description structure that describes the input to the effect.
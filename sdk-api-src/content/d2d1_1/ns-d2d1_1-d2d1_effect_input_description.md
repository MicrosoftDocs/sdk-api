---
UID: NS:d2d1_1.D2D1_EFFECT_INPUT_DESCRIPTION
title: D2D1_EFFECT_INPUT_DESCRIPTION (d2d1_1.h)
description: Describes features of an effect.
helpviewer_keywords: ["D2D1_EFFECT_INPUT_DESCRIPTION","D2D1_EFFECT_INPUT_DESCRIPTION structure [Direct2D]","PD2D1_EFFECT_INPUT_DESCRIPTION","PD2D1_EFFECT_INPUT_DESCRIPTION structure pointer [Direct2D]","d2d1_1/D2D1_EFFECT_INPUT_DESCRIPTION","d2d1_1/PD2D1_EFFECT_INPUT_DESCRIPTION","direct2d.d2d1_effect_input_description"]
old-location: direct2d\d2d1_effect_input_description.htm
tech.root: Direct2D
ms.assetid: 2ce9405a-e36d-4b9e-b9d2-2a58b78696ac
ms.date: 12/05/2018
ms.keywords: D2D1_EFFECT_INPUT_DESCRIPTION, D2D1_EFFECT_INPUT_DESCRIPTION structure [Direct2D], PD2D1_EFFECT_INPUT_DESCRIPTION, PD2D1_EFFECT_INPUT_DESCRIPTION structure pointer [Direct2D], d2d1_1/D2D1_EFFECT_INPUT_DESCRIPTION, d2d1_1/PD2D1_EFFECT_INPUT_DESCRIPTION, direct2d.d2d1_effect_input_description
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
req.type-library: D2D1.lib
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_EFFECT_INPUT_DESCRIPTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_EFFECT_INPUT_DESCRIPTION
 - d2d1_1/D2D1_EFFECT_INPUT_DESCRIPTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2D1.lib
api_name:
 - D2D1_EFFECT_INPUT_DESCRIPTION
---

## -description

Describes features of an effect.

## -struct-fields

### -field effect

The effect whose input connection is being specified.

### -field inputIndex

The input index of the effect that is being considered.

### -field inputRectangle

The amount of data that would be available on the input. This can be used to query this information when the data is not yet available.

## -remarks

> [!NOTE]
> You shouldn't rely heavily on the input rectangles returned by this structure. They can change due to subtle changes in effect implementations, and due to optimization changes in the effect rendering system.


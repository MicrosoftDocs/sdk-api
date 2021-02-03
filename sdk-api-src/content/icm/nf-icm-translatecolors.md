---
UID: NF:icm.TranslateColors
title: TranslateColors
description: Translates an array of colors from the source [color space](c.md) to the destination color space as defined by a color transform.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Mscms.dll
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Mscms.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - 
api_location:
 - Mscms.dll
api_name:
 - TranslateColors
f1_keywords:
 - TranslateColors
 - icm/TranslateColors
dev_langs:
 - c++
---

## -description

Translates an array of colors from the source [color space](c.md) to the destination color space as defined by a color transform.

## -parameters

### -param hColorTransform

Identifies the color transform to use.

### -param paInputColors

Pointer to an array of *nColors*[**COLOR**](color.md) structures to translate.

### -param nColors

Contains the number of elements in the arrays pointed to by *paInputColors* and *paOutputColors*.

### -param ctInput

Specifies the input color type.

### -param paOutputColors

Pointer to an array of *nColors* **COLOR** structures that receive the translated colors.

### -param ctOutput

Specifies the output color type.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

If the input and the output color types are not compatible with the color transform, this function fails.

## -see-also

* [Basic color management concepts](ms536813\(v=vs.85\).md)
* [Functions](ms536536\(v=vs.85\).md)

---
UID: NS:mfobjects._MFOffset
title: MFOffset (mfobjects.h)
description: Specifies an offset as a fixed-point real number.
helpviewer_keywords: ["MFOffset","MFOffset structure [Media Foundation]","e93539fe-3e4a-4b34-8d6a-b3f300a70ffc","mf.mfoffset","mfobjects/MFOffset"]
old-location: mf\mfoffset.htm
tech.root: mf
ms.assetid: e93539fe-3e4a-4b34-8d6a-b3f300a70ffc
ms.date: 12/05/2018
ms.keywords: MFOffset, MFOffset structure [Media Foundation], e93539fe-3e4a-4b34-8d6a-b3f300a70ffc, mf.mfoffset, mfobjects/MFOffset
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFOffset
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFOffset
 - mfobjects/_MFOffset
 - MFOffset
 - mfobjects/MFOffset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MFOffset
---

# MFOffset structure


## -description

Specifies an offset as a fixed-point real number.

## -struct-fields

### -field fract

The fractional part of the number.

### -field value

The integer part of the number.

## -remarks

The value of the number is <b>value</b> + (<b>fract</b> / 65536.0f).


#### Examples


```cpp
MFOffset MakeOffset(float v)
{
    MFOffset offset;
    offset.value = short(v);
    offset.fract = WORD(65536 * (v-offset.value));
    return offset;
}

```

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>
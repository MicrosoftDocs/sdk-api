---
UID: NS:icm.tagCOLOR
title: COLOR
tech.root: wcs
description: Description of the COLOR union.
ms.date: 02/01/2021
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: icm.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
req.target-type: 
req.typenames: COLOR
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - icm.h
api_name:
 - tagCOLOR
 - COLOR
f1_keywords:
 - tagCOLOR
 - icm/tagCOLOR
 - COLOR
 - icm/COLOR
dev_langs:
 - c++
---

## -description

Description of the COLOR union.

## -struct-fields

### -field gray

TBD

### -field rgb

TBD

### -field cmyk

TBD

### -field XYZ

TBD

### -field Yxy

TBD

### -field Lab

TBD

### -field gen3ch

TBD

### -field named

TBD

### -field hifi

TBD

### -field reserved1

TBD

### -field reserved2

TBD

## -remarks

A variable of type COLOR may be accessed as any of the supported color space colors by accessing the appropriate member of the union. For instance, given the following variable declaration:

`COLOR aColor;`

the red, green and blue values could be set in the following manner:

`aColor.rgb.red=100;`

`aColor.rgb.green=50;`

`aColor.rgb.blue=2;`

## -see-also

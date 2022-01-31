---
UID: NE:dwrite_1.DWRITE_PANOSE_WEIGHT
title: DWRITE_PANOSE_WEIGHT (dwrite_1.h)
description: The DWRITE_PANOSE_WEIGHT enumeration contains values that specify the weight of characters.
helpviewer_keywords: ["DWRITE_PANOSE_WEIGHT","DWRITE_PANOSE_WEIGHT enumeration [Direct Write]","DWRITE_PANOSE_WEIGHT_ANY","DWRITE_PANOSE_WEIGHT_BLACK","DWRITE_PANOSE_WEIGHT_BOLD","DWRITE_PANOSE_WEIGHT_BOOK","DWRITE_PANOSE_WEIGHT_DEMI","DWRITE_PANOSE_WEIGHT_EXTRA_BLACK","DWRITE_PANOSE_WEIGHT_HEAVY","DWRITE_PANOSE_WEIGHT_LIGHT","DWRITE_PANOSE_WEIGHT_MEDIUM","DWRITE_PANOSE_WEIGHT_NORD","DWRITE_PANOSE_WEIGHT_NO_FIT","DWRITE_PANOSE_WEIGHT_THIN","DWRITE_PANOSE_WEIGHT_VERY_LIGHT","directwrite.dwrite_panose_weight","dwrite_1/DWRITE_PANOSE_WEIGHT","dwrite_1/DWRITE_PANOSE_WEIGHT_ANY","dwrite_1/DWRITE_PANOSE_WEIGHT_BLACK","dwrite_1/DWRITE_PANOSE_WEIGHT_BOLD","dwrite_1/DWRITE_PANOSE_WEIGHT_BOOK","dwrite_1/DWRITE_PANOSE_WEIGHT_DEMI","dwrite_1/DWRITE_PANOSE_WEIGHT_EXTRA_BLACK","dwrite_1/DWRITE_PANOSE_WEIGHT_HEAVY","dwrite_1/DWRITE_PANOSE_WEIGHT_LIGHT","dwrite_1/DWRITE_PANOSE_WEIGHT_MEDIUM","dwrite_1/DWRITE_PANOSE_WEIGHT_NORD","dwrite_1/DWRITE_PANOSE_WEIGHT_NO_FIT","dwrite_1/DWRITE_PANOSE_WEIGHT_THIN","dwrite_1/DWRITE_PANOSE_WEIGHT_VERY_LIGHT"]
old-location: directwrite\dwrite_panose_weight.htm
tech.root: DirectWrite
ms.assetid: 9309C68B-1193-47EF-A577-9DC0EEE18F4C
ms.date: 12/05/2018
ms.keywords: DWRITE_PANOSE_WEIGHT, DWRITE_PANOSE_WEIGHT enumeration [Direct Write], DWRITE_PANOSE_WEIGHT_ANY, DWRITE_PANOSE_WEIGHT_BLACK, DWRITE_PANOSE_WEIGHT_BOLD, DWRITE_PANOSE_WEIGHT_BOOK, DWRITE_PANOSE_WEIGHT_DEMI, DWRITE_PANOSE_WEIGHT_EXTRA_BLACK, DWRITE_PANOSE_WEIGHT_HEAVY, DWRITE_PANOSE_WEIGHT_LIGHT, DWRITE_PANOSE_WEIGHT_MEDIUM, DWRITE_PANOSE_WEIGHT_NORD, DWRITE_PANOSE_WEIGHT_NO_FIT, DWRITE_PANOSE_WEIGHT_THIN, DWRITE_PANOSE_WEIGHT_VERY_LIGHT, directwrite.dwrite_panose_weight, dwrite_1/DWRITE_PANOSE_WEIGHT, dwrite_1/DWRITE_PANOSE_WEIGHT_ANY, dwrite_1/DWRITE_PANOSE_WEIGHT_BLACK, dwrite_1/DWRITE_PANOSE_WEIGHT_BOLD, dwrite_1/DWRITE_PANOSE_WEIGHT_BOOK, dwrite_1/DWRITE_PANOSE_WEIGHT_DEMI, dwrite_1/DWRITE_PANOSE_WEIGHT_EXTRA_BLACK, dwrite_1/DWRITE_PANOSE_WEIGHT_HEAVY, dwrite_1/DWRITE_PANOSE_WEIGHT_LIGHT, dwrite_1/DWRITE_PANOSE_WEIGHT_MEDIUM, dwrite_1/DWRITE_PANOSE_WEIGHT_NORD, dwrite_1/DWRITE_PANOSE_WEIGHT_NO_FIT, dwrite_1/DWRITE_PANOSE_WEIGHT_THIN, dwrite_1/DWRITE_PANOSE_WEIGHT_VERY_LIGHT
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
 - DWRITE_PANOSE_WEIGHT
 - dwrite_1/DWRITE_PANOSE_WEIGHT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwrite_1.h
api_name:
 - DWRITE_PANOSE_WEIGHT
---

# DWRITE_PANOSE_WEIGHT enumeration


## -description

The <b>DWRITE_PANOSE_WEIGHT</b> enumeration contains values that specify the weight of characters.

## -enum-fields

### -field DWRITE_PANOSE_WEIGHT_ANY:0

Any weight.

### -field DWRITE_PANOSE_WEIGHT_NO_FIT:1

No fit weight.

### -field DWRITE_PANOSE_WEIGHT_VERY_LIGHT:2

Very light weight.

### -field DWRITE_PANOSE_WEIGHT_LIGHT:3

Light weight.

### -field DWRITE_PANOSE_WEIGHT_THIN:4

Thin weight.

### -field DWRITE_PANOSE_WEIGHT_BOOK:5

Book weight.

### -field DWRITE_PANOSE_WEIGHT_MEDIUM:6

Medium weight.

### -field DWRITE_PANOSE_WEIGHT_DEMI:7

Demi weight.

### -field DWRITE_PANOSE_WEIGHT_BOLD:8

Bold weight.

### -field DWRITE_PANOSE_WEIGHT_HEAVY:9

Heavy weight.

### -field DWRITE_PANOSE_WEIGHT_BLACK:10

Black weight.

### -field DWRITE_PANOSE_WEIGHT_EXTRA_BLACK:11

Extra black weight.

### -field DWRITE_PANOSE_WEIGHT_NORD

Extra black weight.

## -remarks

The <b>DWRITE_PANOSE_WEIGHT</b> values roughly correspond to the <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight">DWRITE_FONT_WEIGHT</a> values by using (panose_weight - 2) * 100 = font_weight.

## -see-also

<a href="/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose">DWRITE_PANOSE</a>


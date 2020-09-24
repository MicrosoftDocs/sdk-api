---
UID: NS:rectypes.tagCHARACTER_RANGE
title: CHARACTER_RANGE (rectypes.h)
description: Specifies a range of Unicode points (characters).
helpviewer_keywords: ["*PCHARACTER_RANGE","51d13adf-170e-4172-b752-c9dac5a96fa5","CHARACTER_RANGE","CHARACTER_RANGE structure [Tablet PC]","rectypes/CHARACTER_RANGE","tablet.character_range"]
old-location: tablet\character_range.htm
tech.root: tablet
ms.assetid: 51d13adf-170e-4172-b752-c9dac5a96fa5
ms.date: 12/05/2018
ms.keywords: '*PCHARACTER_RANGE, 51d13adf-170e-4172-b752-c9dac5a96fa5, CHARACTER_RANGE, CHARACTER_RANGE structure [Tablet PC], rectypes/CHARACTER_RANGE, tablet.character_range'
req.header: rectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: CHARACTER_RANGE, *PCHARACTER_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCHARACTER_RANGE
 - rectypes/tagCHARACTER_RANGE
 - PCHARACTER_RANGE
 - rectypes/PCHARACTER_RANGE
 - CHARACTER_RANGE
 - rectypes/CHARACTER_RANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - rectypes.h
api_name:
 - CHARACTER_RANGE
---

# CHARACTER_RANGE structure


## -description

Specifies a range of Unicode points (characters).

## -struct-fields

### -field wcLow

 The low Unicode code point in the range of supported Unicode points.

### -field cChars

 The number of supported Unicode points in this range.

## -see-also

<a href="/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges">GetEnabledUnicodeRanges Function</a>



<a href="/windows/desktop/api/recapis/nf-recapis-getunicoderanges">GetUnicodeRanges Function</a>



<a href="/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges">SetEnabledUnicodeRanges Function</a>
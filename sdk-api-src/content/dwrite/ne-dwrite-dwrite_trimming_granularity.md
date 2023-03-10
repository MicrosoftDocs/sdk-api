---
UID: NE:dwrite.DWRITE_TRIMMING_GRANULARITY
title: DWRITE_TRIMMING_GRANULARITY (dwrite.h)
description: Specifies the text granularity used to trim text overflowing the layout box.
helpviewer_keywords: ["DWRITE_TRIMMING_GRANULARITY","DWRITE_TRIMMING_GRANULARITY enumeration [Direct Write]","DWRITE_TRIMMING_GRANULARITY_CHARACTER","DWRITE_TRIMMING_GRANULARITY_NONE","DWRITE_TRIMMING_GRANULARITY_WORD","directwrite.dwrite_trimming_granularity","dwrite/DWRITE_TRIMMING_GRANULARITY","dwrite/DWRITE_TRIMMING_GRANULARITY_CHARACTER","dwrite/DWRITE_TRIMMING_GRANULARITY_NONE","dwrite/DWRITE_TRIMMING_GRANULARITY_WORD"]
old-location: directwrite\dwrite_trimming_granularity.htm
tech.root: DirectWrite
ms.assetid: 81ab22cd-7b7f-4db6-9f67-2cafd54f4621
ms.date: 12/05/2018
ms.keywords: DWRITE_TRIMMING_GRANULARITY, DWRITE_TRIMMING_GRANULARITY enumeration [Direct Write], DWRITE_TRIMMING_GRANULARITY_CHARACTER, DWRITE_TRIMMING_GRANULARITY_NONE, DWRITE_TRIMMING_GRANULARITY_WORD, directwrite.dwrite_trimming_granularity, dwrite/DWRITE_TRIMMING_GRANULARITY, dwrite/DWRITE_TRIMMING_GRANULARITY_CHARACTER, dwrite/DWRITE_TRIMMING_GRANULARITY_NONE, dwrite/DWRITE_TRIMMING_GRANULARITY_WORD
req.header: dwrite.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_TRIMMING_GRANULARITY
 - dwrite/DWRITE_TRIMMING_GRANULARITY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_TRIMMING_GRANULARITY
---

# DWRITE_TRIMMING_GRANULARITY enumeration


## -description

Specifies  the text granularity used to trim text overflowing the layout box.

## -enum-fields

### -field DWRITE_TRIMMING_GRANULARITY_NONE

No trimming occurs. Text flows beyond the layout width.

### -field DWRITE_TRIMMING_GRANULARITY_CHARACTER

Trimming occurs at a character cluster boundary.

### -field DWRITE_TRIMMING_GRANULARITY_WORD

Trimming occurs at a word boundary.


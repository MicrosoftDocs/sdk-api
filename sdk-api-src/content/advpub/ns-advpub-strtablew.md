---
UID: NS:advpub._StrTableW
title: STRTABLEW (advpub.h)
description: Represents a table of registry string replacements. (Unicode)
helpviewer_keywords: ["*LPSTRTABLEW","LPSTRTABLEW","LPSTRTABLEW structure pointer [Windows API]","STRTABLE","STRTABLEW","STRTABLEW structure [Windows API]","_StrTableW","_StrTableW structure [Windows API]","advpub/LPSTRTABLEW","advpub/_StrTableW","winprog._strtablew"]
old-location: winprog\_strtablew.htm
tech.root: winprog
ms.assetid: 60CE245D-1572-46FC-B3E3-7CE421599E0E
ms.date: 12/05/2018
ms.keywords: '*LPSTRTABLEW, LPSTRTABLEW, LPSTRTABLEW structure pointer [Windows API], STRTABLE, STRTABLEW, STRTABLEW structure [Windows API], _StrTableW, _StrTableW structure [Windows API], advpub/LPSTRTABLEW, advpub/_StrTableW, winprog._strtablew'
req.header: advpub.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Advpack.lib
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: STRTABLEW, *LPSTRTABLEW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _StrTableW
 - advpub/_StrTableW
 - LPSTRTABLEW
 - advpub/LPSTRTABLEW
 - STRTABLEW
 - advpub/STRTABLEW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - advpack.lib
api_name:
 - STRTABLEW
---

# STRTABLEW structure


## -description

Represents a table of registry string replacements.

## -struct-fields

### -field cEntries

The number of entries in the table.

### -field pse

And array of entries.

## -remarks

> [!NOTE]
> The advpub.h header defines STRTABLE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).


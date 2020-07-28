---
UID: NS:advpub._StrTableA
title: STRTABLEA (advpub.h)
description: Represents a table of registry string replacements.
helpviewer_keywords: ["*LPSTRTABLEA","LPSTRTABLEA","LPSTRTABLEA structure pointer [Windows API]","STRTABLE","STRTABLEA","STRTABLEA structure [Windows API]","_StrTableA","_StrTableA structure [Windows API]","advpub/LPSTRTABLEA","advpub/_StrTableA","winprog._strtablea"]
old-location: winprog\_strtablea.htm
tech.root: winprog
ms.assetid: BCDD9AE4-6ADF-4018-A9C0-7924DE30B954
ms.date: 12/05/2018
ms.keywords: '*LPSTRTABLEA, LPSTRTABLEA, LPSTRTABLEA structure pointer [Windows API], STRTABLE, STRTABLEA, STRTABLEA structure [Windows API], _StrTableA, _StrTableA structure [Windows API], advpub/LPSTRTABLEA, advpub/_StrTableA, winprog._strtablea'
f1_keywords:
- advpub/STRTABLEA
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- LibDef
api_location:
- advpack.lib
api_name:
- STRTABLEA
targetos: Windows
req.typenames: STRTABLEA, *LPSTRTABLEA
req.redist: 
ms.custom: 19H1
---

# STRTABLEA structure


## -description


Represents a table of registry string replacements.


## -struct-fields




### -field cEntries

The number of entries in the table.


### -field pse

And array of entries.

## -remarks

> [!NOTE]
> The advpub.h header defines STRTABLE as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).


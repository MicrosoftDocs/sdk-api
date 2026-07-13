---
UID: NS:advpub._StrEntryA
title: STRENTRYA (advpub.h)
description: Represents a registry string replacement. (ANSI)
helpviewer_keywords: ["*LPSTRENTRYA","LPSTRENTRYA","LPSTRENTRYA structure pointer [Windows API]","STRENTRY","STRENTRYA","STRENTRYA structure [Windows API]","_StrEntryA","_StrEntryA structure [Windows API]","advpub/LPSTRENTRYA","advpub/_StrEntryA","winprog._strentrya"]
old-location: winprog\_strentrya.htm
tech.root: winprog
ms.assetid: BE4239CA-68D5-4E5A-BA53-087001ACD7BB
ms.date: 12/05/2018
ms.keywords: '*LPSTRENTRYA, LPSTRENTRYA, LPSTRENTRYA structure pointer [Windows API], STRENTRY, STRENTRYA, STRENTRYA structure [Windows API], _StrEntryA, _StrEntryA structure [Windows API], advpub/LPSTRENTRYA, advpub/_StrEntryA, winprog._strentrya'
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
req.typenames: STRENTRYA, *LPSTRENTRYA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _StrEntryA
 - advpub/_StrEntryA
 - LPSTRENTRYA
 - advpub/LPSTRENTRYA
 - STRENTRYA
 - advpub/STRENTRYA
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
 - STRENTRYA
---

# STRENTRYA structure


## -description

Represents a registry string replacement.

## -struct-fields

### -field pszName

The name of the string to substitute.

### -field pszValue

The replacement string.

## -remarks

> [!NOTE]
> The advpub.h header defines STRENTRY as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).


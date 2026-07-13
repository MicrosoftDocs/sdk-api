---
UID: NS:advpub._StrEntryW
title: STRENTRYW (advpub.h)
description: Represents a registry string replacement. (Unicode)
helpviewer_keywords: ["*LPSTRENTRYW","LPSTRENTRYW","LPSTRENTRYW structure pointer [Windows API]","STRENTRY","STRENTRYW","STRENTRYW structure [Windows API]","_StrEntryW","_StrEntryW structure [Windows API]","advpub/LPSTRENTRYW","advpub/_StrEntryW","winprog._strentryw"]
old-location: winprog\_strentryw.htm
tech.root: winprog
ms.assetid: 0EA85285-B5CC-4DC2-ADB7-4888316634C3
ms.date: 12/05/2018
ms.keywords: '*LPSTRENTRYW, LPSTRENTRYW, LPSTRENTRYW structure pointer [Windows API], STRENTRY, STRENTRYW, STRENTRYW structure [Windows API], _StrEntryW, _StrEntryW structure [Windows API], advpub/LPSTRENTRYW, advpub/_StrEntryW, winprog._strentryw'
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
req.typenames: STRENTRYW, *LPSTRENTRYW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _StrEntryW
 - advpub/_StrEntryW
 - LPSTRENTRYW
 - advpub/LPSTRENTRYW
 - STRENTRYW
 - advpub/STRENTRYW
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
 - STRENTRYW
---

# STRENTRYW structure


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


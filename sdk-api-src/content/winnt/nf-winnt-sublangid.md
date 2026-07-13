---
UID: NF:winnt.SUBLANGID
title: SUBLANGID macro (winnt.h)
description: Extracts a sublanguage identifier from a language identifier.
helpviewer_keywords: ["SUBLANGID","SUBLANGID macro [Internationalization for Windows Applications]","_win32_SUBLANGID","intl.sublangid","winnt/SUBLANGID"]
old-location: intl\sublangid.htm
tech.root: Intl
ms.assetid: 0441c915-f910-4ac7-ac0a-0b113f490d40
ms.date: 07/01/2025
ms.keywords: SUBLANGID, SUBLANGID macro [Internationalization for Windows Applications], _win32_SUBLANGID, intl.sublangid, winnt/SUBLANGID
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - SUBLANGID
 - winnt/SUBLANGID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - SUBLANGID
---

# SUBLANGID macro

## -syntax

```cpp
WORD SUBLANGID(
    WORD lgid
);
```

## -returns

Type: **WORD**

Returns a sublanguage identifier. This can be a predefined sublanguage identifier or a user-defined sublanguage identifier.


## -description

Extracts a sublanguage identifier from a <a href="/windows/desktop/Intl/language-identifiers">language identifier</a>.

## -parameters

### -param lgid

Language identifier. You can supply predefined values for this parameter, or create an identifier using the <a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a> macro.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesa">EnumSystemLocales</a>



<a href="/windows/desktop/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a>



<a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-macros">National Language Support Macros</a>



<a href="/windows/desktop/api/winnt/nf-winnt-primarylangid">PRIMARYLANGID</a>

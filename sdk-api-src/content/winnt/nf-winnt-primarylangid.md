---
UID: NF:winnt.PRIMARYLANGID
title: PRIMARYLANGID macro (winnt.h)
description: Extracts a primary language identifier from a language identifier.
helpviewer_keywords: ["PRIMARYLANGID","PRIMARYLANGID macro [Internationalization for Windows Applications]","_win32_PRIMARYLANGID","intl.primarylangid","winnt/PRIMARYLANGID"]
old-location: intl\primarylangid.htm
tech.root: Intl
ms.assetid: e463a2dc-bf36-4fbb-8df6-799ca1d549fa
ms.date: 07/01/2025
ms.keywords: PRIMARYLANGID, PRIMARYLANGID macro [Internationalization for Windows Applications], _win32_PRIMARYLANGID, intl.primarylangid, winnt/PRIMARYLANGID
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
 - PRIMARYLANGID
 - winnt/PRIMARYLANGID
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
 - PRIMARYLANGID
---

# PRIMARYLANGID macro

## -syntax

```cpp
WORD PRIMARYLANGID(
    WORD lgid
);
```

## -returns

Type: **WORD**

Returns the primary language identifier. It can be one of the predefined primary language identifiers or a user-defined primary language identifier. For more information, see <a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a>.


## -description

Extracts a primary language identifier from a <a href="/windows/desktop/Intl/language-identifiers">language identifier</a>.

## -parameters

### -param lgid

Language identifier. This value is a combination of a primary language identifier and a sublanguage identifier and is usually created by using the <a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a> macro.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-enumsystemlocalesa">EnumSystemLocales</a>



<a href="/windows/desktop/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a>



<a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-macros">National Language Support Macros</a>



<a href="/windows/desktop/api/winnt/nf-winnt-sublangid">SUBLANGID</a>

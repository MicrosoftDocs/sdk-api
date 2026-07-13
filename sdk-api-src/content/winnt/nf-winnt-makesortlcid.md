---
UID: NF:winnt.MAKESORTLCID
title: MAKESORTLCID macro (winnt.h)
description: Constructs a locale identifier (LCID) from a language identifier, a sort order identifier, and the sort version.
helpviewer_keywords: ["MAKESORTLCID","MAKESORTLCID macro [Internationalization for Windows Applications]","_win32_MAKESORTLCID","intl.makesortlcid","winnt/MAKESORTLCID"]
old-location: intl\makesortlcid.htm
tech.root: Intl
ms.assetid: 58327bfc-8a00-4fdc-bd5a-cef9c0b29faa
ms.date: 07/01/2025
ms.keywords: MAKESORTLCID, MAKESORTLCID macro [Internationalization for Windows Applications], _win32_MAKESORTLCID, intl.makesortlcid, winnt/MAKESORTLCID
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
 - MAKESORTLCID
 - winnt/MAKESORTLCID
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
 - MAKESORTLCID
---

# MAKESORTLCID macro

## -syntax

```cpp
DWORD MAKESORTLCID(
    WORD lgid,
    WORD srtid,
    WORD ver
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns the LCID.


## -description

Constructs a <a href="/windows/desktop/Intl/locale-identifiers">locale identifier</a> (LCID) from a <a href="/windows/desktop/Intl/language-identifiers">language identifier</a>, a <a href="/windows/desktop/Intl/sort-order-identifiers">sort order identifier</a>, and the sort version.

## -parameters

### -param lgid

Language identifier. This parameter is a combination of a primary language identifier and a sublanguage identifier and is usually created by using the <a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a> macro.

### -param srtid

Sort order identifier.

### -param ver

Reserved; must be 0.

## -remarks

<a href="/windows/desktop/Intl/locale-invariant">LOCALE_INVARIANT</a> represents a special locale-independent locale identifier. It is designed for system-level functions that require consistent results regardless of the locale that the user has chosen, for example, sorting in the file system. Typically, an application does not use LOCALE_INVARIANT because it expects the results of an action to depend on the rules governing each individual locale.


<a href="/windows/desktop/Intl/locale-invariant">LOCALE_INVARIANT</a> is composed of a language identifier consisting of LANG_INVARIANT for the primary language and SUBLANG_NEUTRAL for the sublanguage. SORT_DEFAULT is used for the sort order identifier.

## -see-also

<a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-macros">National Language Support Macros</a>

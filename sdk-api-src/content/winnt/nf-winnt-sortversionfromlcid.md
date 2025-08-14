---
UID: NF:winnt.SORTVERSIONFROMLCID
title: SORTVERSIONFROMLCID macro (winnt.h)
description: Retrieves the sort version from a locale identifier.
helpviewer_keywords: ["SORTVERSIONFROMLCID","SORTVERSIONFROMLCID macro [Internationalization for Windows Applications]","_win32_SORTVERSIONFROMLCID","intl.sortversionfromlcid","winnt/SORTVERSIONFROMLCID"]
old-location: intl\sortversionfromlcid.htm
tech.root: Intl
ms.assetid: 2a851ec1-ccb9-42d3-bbb5-70cb9cf02cc7
ms.date: 07/01/2025
ms.keywords: SORTVERSIONFROMLCID, SORTVERSIONFROMLCID macro [Internationalization for Windows Applications], _win32_SORTVERSIONFROMLCID, intl.sortversionfromlcid, winnt/SORTVERSIONFROMLCID
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
 - SORTVERSIONFROMLCID
 - winnt/SORTVERSIONFROMLCID
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
 - SORTVERSIONFROMLCID
---

# SORTVERSIONFROMLCID macro

## -syntax

```cpp
WORD SORTVERSIONFROMLCID(
    LCID lcid
);
```

## -returns

Type: **WORD**

Returns the sort version. Currently, this macro only returns 0.


## -description

Retrieves the sort version from a <a href="/windows/desktop/Intl/locale-identifiers">locale identifier</a>.

## -parameters

### -param lcid

Locale identifier. You can use the <a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a> macro to create a locale identifier or use one of the following predefined values. 

<ul>
<li>
<a href="/windows/desktop/Intl/locale-invariant">LOCALE_INVARIANT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-system-default">LOCALE_SYSTEM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-user-default">LOCALE_USER_DEFAULT</a>
</li>
</ul>
<b>Windows Vista and later:</b> The following custom locale identifiers are also supported.

<ul>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UI_DEFAULT</a>
</li>
<li>
<a href="/windows/desktop/Intl/locale-custom-constants">LOCALE_CUSTOM_UNSPECIFIED</a>
</li>
</ul>

## -remarks

Note that this macro is entirely distinct from <a href="/windows/desktop/api/winnt/nf-winnt-sortidfromlcid">SORTIDFROMLCID</a>.

## -see-also

<a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-macros">National Language Support Macros</a>



<a href="/windows/desktop/api/winnt/nf-winnt-sortidfromlcid">SORTIDFROMLCID</a>

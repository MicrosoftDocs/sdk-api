---
UID: NF:winnt.SORTIDFROMLCID
title: SORTIDFROMLCID macro (winnt.h)
description: Retrieves a sort order identifier from a locale identifier.
helpviewer_keywords: ["SORTIDFROMLCID","SORTIDFROMLCID macro [Internationalization for Windows Applications]","_win32_SORTIDFROMLCID","intl.sortidfromlcid","winnt/SORTIDFROMLCID"]
old-location: intl\sortidfromlcid.htm
tech.root: Intl
ms.assetid: 78da443e-ad92-4e2f-aebe-c0aed880b8b6
ms.date: 07/01/2025
ms.keywords: SORTIDFROMLCID, SORTIDFROMLCID macro [Internationalization for Windows Applications], _win32_SORTIDFROMLCID, intl.sortidfromlcid, winnt/SORTIDFROMLCID
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
 - SORTIDFROMLCID
 - winnt/SORTIDFROMLCID
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
 - SORTIDFROMLCID
---

# SORTIDFROMLCID macro

## -syntax

```cpp
WORD SORTIDFROMLCID(
    LCID lcid
);
```

## -returns

Type: **WORD**

Returns a sort order identifier.


## -description

Retrieves a <a href="/windows/desktop/Intl/sort-order-identifiers">sort order identifier</a> from a <a href="/windows/desktop/Intl/locale-identifiers">locale identifier</a>.

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

## -see-also

<a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a>



<a href="/windows/desktop/api/winnt/nf-winnt-makelcid">MAKELCID</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-macros">National Language Support Macros</a>



<a href="/windows/desktop/api/winnt/nf-winnt-primarylangid">PRIMARYLANGID</a>



<a href="/windows/desktop/api/winnt/nf-winnt-sublangid">SUBLANGID</a>

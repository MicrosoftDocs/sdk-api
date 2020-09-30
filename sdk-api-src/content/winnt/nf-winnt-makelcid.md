---
UID: NF:winnt.MAKELCID
title: MAKELCID macro (winnt.h)
description: Creates a locale identifier from a language identifier and a sort order identifier.
helpviewer_keywords: ["MAKELCID","MAKELCID macro [Internationalization for Windows Applications]","_win32_MAKELCID","intl.makelcid","winnt/MAKELCID"]
old-location: intl\makelcid.htm
tech.root: Intl
ms.assetid: 2f8893a0-f916-4a62-a423-e525cf281fa4
ms.date: 12/05/2018
ms.keywords: MAKELCID, MAKELCID macro [Internationalization for Windows Applications], _win32_MAKELCID, intl.makelcid, winnt/MAKELCID
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
 - MAKELCID
 - winnt/MAKELCID
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
 - MAKELCID
---

# MAKELCID macro


## -description

Creates a <a href="/windows/desktop/Intl/locale-identifiers">locale identifier</a> from a <a href="/windows/desktop/Intl/language-identifiers">language identifier</a> and a <a href="/windows/desktop/Intl/sort-order-identifiers">sort order identifier</a>.

## -parameters

### -param lgid

Language identifier. This identifier is a combination of a primary language identifier and a sublanguage identifier and is usually created by using the <a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a> macro.

### -param srtid

Sort order identifier.

## -see-also

<a href="/windows/desktop/api/winnt/nf-winnt-langidfromlcid">LANGIDFROMLCID</a>



<a href="/windows/desktop/api/winnt/nf-winnt-makelangid">MAKELANGID</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-macros">National Language Support Macros</a>



<a href="/windows/desktop/api/winnt/nf-winnt-sortidfromlcid">SORTIDFROMLCID</a>
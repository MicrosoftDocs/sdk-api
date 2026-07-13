---
UID: NS:wingdi.tagCHARSETINFO
title: CHARSETINFO (wingdi.h)
description: Contains information about a character set.
helpviewer_keywords: ["*LPCHARSETINFO","*NPCHARSETINFO","*PCHARSETINFO","CHARSETINFO","CHARSETINFO structure [Internationalization for Windows Applications]","PCHARSETINFO","PCHARSETINFO structure pointer [Internationalization for Windows Applications]","_win32_CHARSETINFO_str","intl.charsetinfo","wingdi/CHARSETINFO","wingdi/PCHARSETINFO"]
old-location: intl\charsetinfo.htm
tech.root: Intl
ms.assetid: 4f815f53-9fac-41f3-9493-bd8d68cff543
ms.date: 12/05/2018
ms.keywords: '*LPCHARSETINFO, *NPCHARSETINFO, *PCHARSETINFO, CHARSETINFO, CHARSETINFO structure [Internationalization for Windows Applications], PCHARSETINFO, PCHARSETINFO structure pointer [Internationalization for Windows Applications], _win32_CHARSETINFO_str, intl.charsetinfo, wingdi/CHARSETINFO, wingdi/PCHARSETINFO'
req.header: wingdi.h
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
req.typenames: CHARSETINFO, *PCHARSETINFO, *NPCHARSETINFO, *LPCHARSETINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCHARSETINFO
 - wingdi/tagCHARSETINFO
 - PCHARSETINFO
 - wingdi/PCHARSETINFO
 - CHARSETINFO
 - wingdi/CHARSETINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - CHARSETINFO
---

# CHARSETINFO structure


## -description

Contains information about a character set.

## -struct-fields

### -field ciCharset

Character set value. For a list of possible values, see *lfCharSet* field of the <a href="/windows/desktop/api/wingdi/ns-wingdi-logfontw">LOGFONT structure</a>.

### -field ciACP

Windows ANSI code page identifier. For a list of identifiers, see <a href="/windows/desktop/Intl/code-page-identifiers">Code Page Identifiers</a>.

### -field fs

A <a href="/windows/desktop/api/wingdi/ns-wingdi-fontsignature">FONTSIGNATURE</a> structure that identifies the Unicode subrange and the specific Windows ANSI character set/code page. Only one code page will be set when this structure is set by the function.

## -see-also

<a href="/windows/desktop/Intl/code-pages">Code Pages</a>

<a href="/windows/desktop/api/wingdi/ns-wingdi-fontsignature">FONTSIGNATURE</a>

<a href="/windows/desktop/api/wingdi/ns-wingdi-logfontw">LOGFONT</a>

<a href="/windows/desktop/api/wingdi/nf-wingdi-translatecharsetinfo">TranslateCharsetInfo</a>

<a href="/windows/desktop/Intl/unicode-and-character-set-structures">Unicode and Character Set Structures</a>

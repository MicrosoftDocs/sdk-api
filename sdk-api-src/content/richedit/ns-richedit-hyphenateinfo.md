---
UID: NS:richedit.tagHyphenateInfo
title: HYPHENATEINFO (richedit.h)
description: Contains information about hyphenation in a Microsoft Rich Edit control.
helpviewer_keywords: ["HYPHENATEINFO","HYPHENATEINFO structure [Windows Controls]","_win32_HYPHENATEINFO_str","_win32_HYPHENATEINFO_str_cpp","controls.HYPHENATEINFO","controls._win32_HYPHENATEINFO_str","richedit/HYPHENATEINFO"]
old-location: controls\HYPHENATEINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\hyphenateinfo.htm
ms.date: 12/05/2018
ms.keywords: HYPHENATEINFO, HYPHENATEINFO structure [Windows Controls], _win32_HYPHENATEINFO_str, _win32_HYPHENATEINFO_str_cpp, controls.HYPHENATEINFO, controls._win32_HYPHENATEINFO_str, richedit/HYPHENATEINFO
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: HYPHENATEINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHyphenateInfo
 - richedit/tagHyphenateInfo
 - HYPHENATEINFO
 - richedit/HYPHENATEINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - HYPHENATEINFO
---

# HYPHENATEINFO structure


## -description

Contains information about hyphenation in a Microsoft Rich Edit control.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SHORT</a></b>

Size of the <b>HYPHENATEINFO</b> structure, in bytes.

### -field dxHyphenateZone

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SHORT</a></b>

Size, in TWIPS (one TWIP is 1/1440 inch), of the area near the margin that excludes hyphenation. If a space character is closer to the margin than this value, do not hyphenate the following word.

### -field pfnHyphenate

Type: <b>PFNHYPHENATEPROC</b>

The client-defined <a href="/windows/win32/api/richedit/nf-richedit-hyphenateproc">HyphenateProc</a> callback function.

## -remarks

This structure is used with the <a href="/windows/win32/controls/em-gethyphenateinfo">EM_GETHYPHENATEINFO</a> and <a href="/windows/win32/controls/em-sethyphenateinfo">EM_SETHYPHENATEINFO</a> messages.

## -see-also

<a href="/windows/win32/controls/em-gethyphenateinfo">EM_GETHYPHENATEINFO</a>



<a href="/windows/win32/controls/em-sethyphenateinfo">EM_SETHYPHENATEINFO</a>



<a href="/windows/win32/api/richedit/nf-richedit-hyphenateproc">HyphenateProc</a>



<b>Reference</b>

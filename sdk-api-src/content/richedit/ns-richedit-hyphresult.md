---
UID: NS:richedit.hyphresult
title: HYPHRESULT (richedit.h)
description: Contains information about the result of hyphenation in a Microsoft Rich Edit control.
helpviewer_keywords: ["HYPHRESULT","HYPHRESULT structure [Windows Controls]","_win32_HYPHRESULT_str","_win32_HYPHRESULT_str_cpp","controls.HYPHRESULT","controls._win32_HYPHRESULT_str","richedit/HYPHRESULT"]
old-location: controls\HYPHRESULT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\hyphresult.htm
ms.date: 12/05/2018
ms.keywords: HYPHRESULT, HYPHRESULT structure [Windows Controls], _win32_HYPHRESULT_str, _win32_HYPHRESULT_str_cpp, controls.HYPHRESULT, controls._win32_HYPHRESULT_str, richedit/HYPHRESULT
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
req.typenames: HYPHRESULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - hyphresult
 - richedit/hyphresult
 - HYPHRESULT
 - richedit/HYPHRESULT
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
 - HYPHRESULT
---

# HYPHRESULT structure


## -description

Contains information about the result of hyphenation in a Microsoft Rich Edit control.

## -struct-fields

### -field khyph

Type: <b><a href="/windows/win32/api/richedit/ne-richedit-khyph">KHYPH</a></b>

The type of hyphenation.

### -field ichHyph

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

The index of the WCHAR in the passed string where hyphenation occurred.

### -field chHyph

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WCHAR</a></b>

The character used when hyphenation requires a replacement or an addition or a change. If no new character is needed, the value is zero.

## -remarks

This structure is used with the <a href="/windows/win32/api/richedit/ns-richedit-hyphenateinfo">HYPHENATEINFO</a> structure.

## -see-also

<a href="/windows/win32/api/richedit/ns-richedit-hyphenateinfo">HYPHENATEINFO</a>



<a href="/windows/win32/api/richedit/ne-richedit-khyph">KHYPH</a>



<b>Reference</b>

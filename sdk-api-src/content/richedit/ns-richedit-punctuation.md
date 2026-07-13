---
UID: NS:richedit._punctuation
title: PUNCTUATION (richedit.h)
description: Contains information about the punctuation used in a rich edit control.
helpviewer_keywords: ["PUNCTUATION","PUNCTUATION structure [Windows Controls]","_win32_PUNCTUATION_str","_win32_PUNCTUATION_str_cpp","controls.PUNCTUATION","controls._win32_PUNCTUATION_str","richedit/PUNCTUATION"]
old-location: controls\PUNCTUATION.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\punctuation.htm
ms.date: 12/05/2018
ms.keywords: PUNCTUATION, PUNCTUATION structure [Windows Controls], _win32_PUNCTUATION_str, _win32_PUNCTUATION_str_cpp, controls.PUNCTUATION, controls._win32_PUNCTUATION_str, richedit/PUNCTUATION
req.header: richedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: PUNCTUATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _punctuation
 - richedit/_punctuation
 - PUNCTUATION
 - richedit/PUNCTUATION
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
 - PUNCTUATION
---

# PUNCTUATION structure


## -description

Contains information about the punctuation used in a rich edit control.

## -struct-fields

### -field iSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of buffer pointed to by the 
					<b>szPunctuation</b> member, in bytes.

### -field szPunctuation

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPSTR</a></b>

The buffer containing the punctuation characters.

## -remarks

This structure is used only in Asian-language versions of the operating system.

## -see-also

<a href="/windows/win32/controls/em-getpunctuation">EM_GETPUNCTUATION</a>



<a href="/windows/win32/controls/em-setpunctuation">EM_SETPUNCTUATION</a>



<b>Reference</b>
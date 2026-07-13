---
UID: NF:richedit.HyphenateProc
title: HyphenateProc function (richedit.h)
description: The HyphenateProc function is an application—defined callback function used with the EM_SETHYPHENATEINFO message. It determines how hyphenation is done in a Microsoft Rich Edit control.
helpviewer_keywords: ["HyphenateProc","HyphenateProc callback","HyphenateProc callback function [Windows Controls]","_win32_HyphenateProc","_win32_HyphenateProc_cpp","controls.HyphenateProc","controls._win32_HyphenateProc","richedit/HyphenateProc"]
old-location: controls\HyphenateProc.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditcallbackfunctions\hyphenateproc.htm
ms.date: 12/05/2018
ms.keywords: HyphenateProc, HyphenateProc callback, HyphenateProc callback function [Windows Controls], _win32_HyphenateProc, _win32_HyphenateProc_cpp, controls.HyphenateProc, controls._win32_HyphenateProc, richedit/HyphenateProc
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HyphenateProc
 - richedit/HyphenateProc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Richedit.h
api_name:
 - HyphenateProc
---

# HyphenateProc function


## -description

The <i>HyphenateProc</i> function is an application–defined
		callback function used with the <a href="/windows/win32/controls/em-sethyphenateinfo">EM_SETHYPHENATEINFO</a> message. It determines how hyphenation is done in a Microsoft Rich Edit control.

## -parameters

### -param pszWord [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WCHAR</a>*</b>

Pointer to the word to hyphenate.

### -param langid [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LANGID</a></b>

Current language ID for the control.

### -param ichExceed [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Index of the character in the passed string that exceeds the line width.

### -param phyphresult [out]

Type: <b><a href="/windows/win32/api/richedit/ns-richedit-hyphresult">HYPHRESULT</a>*</b>

Pointer to a <a href="/windows/win32/api/richedit/ns-richedit-hyphresult">HYPHRESULT</a> structure that <i>HyphenateProc</i> fills in with the result of the hyphenation.

## -remarks

<i>HyphenateProc</i> is a placeholder for the application-defined function name.

An application must install the callback function by specifying the address of the callback function in an <a href="/windows/win32/controls/em-sethyphenateinfo">EM_SETHYPHENATEINFO</a> message.

## -see-also

<a href="/windows/win32/controls/em-sethyphenateinfo">EM_SETHYPHENATEINFO</a>



<a href="/windows/win32/api/richedit/ns-richedit-hyphenateinfo">HYPHENATEINFO</a>



<a href="/windows/win32/api/richedit/ns-richedit-hyphresult">HYPHRESULT</a>



<b>Reference</b>

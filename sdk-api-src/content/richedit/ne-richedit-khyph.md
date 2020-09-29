---
UID: NE:richedit.tagKHYPH
title: KHYPH (richedit.h)
description: Contains values used to specify how to do hyphenation in a rich edit control. The HyphenateProc callback function uses this enumeration type.
helpviewer_keywords: ["KHYPH","KHYPH enumeration [Windows Controls]","_win32_KHYPH","_win32_KHYPH_cpp","controls.KHYPH","controls._win32_KHYPH","khyphAddBefore","khyphChangeAfter","khyphChangeBefore","khyphDelAndChange","khyphDeleteBefore","khyphNil","khyphNormal","richedit/KHYPH","richedit/khyphAddBefore","richedit/khyphChangeAfter","richedit/khyphChangeBefore","richedit/khyphDelAndChange","richedit/khyphDeleteBefore","richedit/khyphNil","richedit/khyphNormal"]
old-location: controls\KHYPH.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditenumerationtypes\khyph.htm
ms.date: 12/05/2018
ms.keywords: KHYPH, KHYPH enumeration [Windows Controls], _win32_KHYPH, _win32_KHYPH_cpp, controls.KHYPH, controls._win32_KHYPH, khyphAddBefore, khyphChangeAfter, khyphChangeBefore, khyphDelAndChange, khyphDeleteBefore, khyphNil, khyphNormal, richedit/KHYPH, richedit/khyphAddBefore, richedit/khyphChangeAfter, richedit/khyphChangeBefore, richedit/khyphDelAndChange, richedit/khyphDeleteBefore, richedit/khyphNil, richedit/khyphNormal
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
req.typenames: KHYPH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagKHYPH
 - richedit/tagKHYPH
 - KHYPH
 - richedit/KHYPH
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
 - KHYPH
---

# KHYPH enumeration


## -description

Contains values used to specify how to do hyphenation in a rich edit control. The <a href="/windows/win32/api/richedit/nf-richedit-hyphenateproc">HyphenateProc</a> callback function uses this enumeration type.

## -enum-fields

### -field khyphNil

No hyphenation is allowed.

### -field khyphNormal

Do not change any characters during hyphenation.

### -field khyphAddBefore

Add a letter before the hyphenation mark.

### -field khyphChangeBefore

Change the letter before the hyphenation mark.

### -field khyphDeleteBefore

Delete the letter before the hyphenation mark.

### -field khyphChangeAfter

Change the letter after the hyphenation mark.

### -field khyphDelAndChange

The two letters before the hyphenation mark are replaced by one character; see the <b>chHyph</b> member of <a href="/windows/win32/api/richedit/ns-richedit-hyphresult">HYPHRESULT</a>.

## -remarks

Hyphenation rules are specific for each language; not all hyphenation types are valid for a given language.

## -see-also

<a href="/windows/win32/api/richedit/ns-richedit-hyphresult">HYPHRESULT</a>



<a href="/windows/win32/api/richedit/nf-richedit-hyphenateproc">HyphenateProc</a>



<b>Reference</b>


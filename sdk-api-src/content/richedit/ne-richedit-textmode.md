---
UID: NE:richedit.tagTextMode
title: TEXTMODE (richedit.h)
description: Indicates the text mode of a rich edit control. The EM_SETTEXTMODE and EM_GETTEXTMODE messages use this enumeration type.
helpviewer_keywords: ["TEXTMODE","TEXTMODE enumeration [Windows Controls]","TM_MULTICODEPAGE","TM_MULTILEVELUNDO","TM_PLAINTEXT","TM_RICHTEXT","TM_SINGLECODEPAGE","TM_SINGLELEVELUNDO","_win32_TEXTMODE_str","_win32_TEXTMODE_str_cpp","controls.TEXTMODE","controls._win32_TEXTMODE_str","richedit/TEXTMODE","richedit/TM_MULTICODEPAGE","richedit/TM_MULTILEVELUNDO","richedit/TM_PLAINTEXT","richedit/TM_RICHTEXT","richedit/TM_SINGLECODEPAGE","richedit/TM_SINGLELEVELUNDO"]
old-location: controls\TEXTMODE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditenumerationtypes\textmode.htm
ms.date: 12/05/2018
ms.keywords: TEXTMODE, TEXTMODE enumeration [Windows Controls], TM_MULTICODEPAGE, TM_MULTILEVELUNDO, TM_PLAINTEXT, TM_RICHTEXT, TM_SINGLECODEPAGE, TM_SINGLELEVELUNDO, _win32_TEXTMODE_str, _win32_TEXTMODE_str_cpp, controls.TEXTMODE, controls._win32_TEXTMODE_str, richedit/TEXTMODE, richedit/TM_MULTICODEPAGE, richedit/TM_MULTILEVELUNDO, richedit/TM_PLAINTEXT, richedit/TM_RICHTEXT, richedit/TM_SINGLECODEPAGE, richedit/TM_SINGLELEVELUNDO
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
req.typenames: TEXTMODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTextMode
 - richedit/tagTextMode
 - TEXTMODE
 - richedit/TEXTMODE
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
 - TEXTMODE
---

# TEXTMODE enumeration


## -description

Indicates the text mode of a rich edit control. The <a href="https://msdn.microsoft.com/d6741234-0ef3-4cd2-8817-6c852f1b500d">EM_SETTEXTMODE</a> and <a href="https://msdn.microsoft.com/5c976a82-9c51-4700-9db4-a6b0ed7bb852">EM_GETTEXTMODE</a> messages use this enumeration type.

## -enum-fields

### -field TM_PLAINTEXT:1

Indicates plain-text mode, in which the control is similar to a standard edit control. For more information about plain-text mode, see the Remarks section of <a href="https://msdn.microsoft.com/d6741234-0ef3-4cd2-8817-6c852f1b500d">EM_SETTEXTMODE</a>.

### -field TM_RICHTEXT:2

Indicates rich-text mode, in which the control has the standard rich edit functionality. Rich-text mode is the default setting.

### -field TM_SINGLELEVELUNDO:4

The control allows the user to undo only the last action in the undo queue.

### -field TM_MULTILEVELUNDO:8

The control supports multiple undo actions. This is the default setting. Use the <a href="https://msdn.microsoft.com/485dbcda-89f4-40de-ad55-cd524958e910">EM_SETUNDOLIMIT</a> message to set the maximum number of undo actions.

### -field TM_SINGLECODEPAGE:16

The control only allows the English keyboard and a keyboard corresponding to the default character set. For example, you could have Greek and English. Note that this prevents Unicode text from entering the control. For example, use this value if a Rich Edit control must be restricted to ANSI text.

### -field TM_MULTICODEPAGE:32	

The control allows multiple code pages and Unicode text into the control. This is the default setting.

## -see-also

<a href="https://msdn.microsoft.com/5c976a82-9c51-4700-9db4-a6b0ed7bb852">EM_GETTEXTMODE</a>



<a href="https://msdn.microsoft.com/d6741234-0ef3-4cd2-8817-6c852f1b500d">EM_SETTEXTMODE</a>



<b>Reference</b>


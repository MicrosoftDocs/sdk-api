---
UID: NE:richedit._undonameid
title: UNDONAMEID (richedit.h)
description: Contains values that indicate types of rich edit control actions that can be undone or redone. The EM_GETREDONAME and EM_GETUNDONAME messages use this enumeration type to return a value.
helpviewer_keywords: ["UID_AUTOTABLE","UID_CUT","UID_DELETE","UID_DRAGDROP","UID_PASTE","UID_TYPING","UID_UNKNOWN","UNDONAMEID","UNDONAMEID enumeration [Windows Controls]","_win32_UNDONAMEID_str","_win32_UNDONAMEID_str_cpp","controls.UNDONAMEID","controls._win32_UNDONAMEID_str","richedit/UID_AUTOTABLE","richedit/UID_CUT","richedit/UID_DELETE","richedit/UID_DRAGDROP","richedit/UID_PASTE","richedit/UID_TYPING","richedit/UID_UNKNOWN","richedit/UNDONAMEID"]
old-location: controls\UNDONAMEID.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditenumerationtypes\undonameid.htm
ms.date: 12/05/2018
ms.keywords: UID_AUTOTABLE, UID_CUT, UID_DELETE, UID_DRAGDROP, UID_PASTE, UID_TYPING, UID_UNKNOWN, UNDONAMEID, UNDONAMEID enumeration [Windows Controls], _win32_UNDONAMEID_str, _win32_UNDONAMEID_str_cpp, controls.UNDONAMEID, controls._win32_UNDONAMEID_str, richedit/UID_AUTOTABLE, richedit/UID_CUT, richedit/UID_DELETE, richedit/UID_DRAGDROP, richedit/UID_PASTE, richedit/UID_TYPING, richedit/UID_UNKNOWN, richedit/UNDONAMEID
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
req.typenames: UNDONAMEID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _undonameid
 - richedit/_undonameid
 - UNDONAMEID
 - richedit/UNDONAMEID
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
 - UNDONAMEID
---

# UNDONAMEID enumeration


## -description

Contains values that indicate types of rich edit control actions that can be undone or redone. The <a href="https://msdn.microsoft.com/8649236f-32dc-45d3-847e-c9f65ffba44c">EM_GETREDONAME</a> and <a href="https://msdn.microsoft.com/43351909-f8bc-425a-9d9b-655e3b47eb75">EM_GETUNDONAME</a> messages use this enumeration type to return a value.

## -enum-fields

### -field UID_UNKNOWN:0

The type of undo action is unknown.

### -field UID_TYPING:1

Typing operation.

### -field UID_DELETE:2

Delete operation.

### -field UID_DRAGDROP:3

Drag-and-drop operation.

### -field UID_CUT:4

Cut operation.

### -field UID_PASTE:5

Paste operation.

### -field UID_AUTOTABLE:6

Automatic table insertion; for example, typing +---+---+&lt;Enter&gt; to insert a table row.

## -see-also

<a href="https://msdn.microsoft.com/8649236f-32dc-45d3-847e-c9f65ffba44c">EM_GETREDONAME</a>



<a href="https://msdn.microsoft.com/43351909-f8bc-425a-9d9b-655e3b47eb75">EM_GETUNDONAME</a>



<b>Reference</b>


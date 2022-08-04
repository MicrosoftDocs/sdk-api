---
UID: NS:immdev.tagCANDIDATELIST
title: CANDIDATELIST (immdev.h)
description: The CANDIDATELIST structure (immdev.h) contains information about a candidate list.
helpviewer_keywords: ["*LPCANDIDATELIST","*NPCANDIDATELIST","*PCANDIDATELIST","CANDIDATELIST","CANDIDATELIST structure [Internationalization for Windows Applications]","PCANDIDATELIST","PCANDIDATELIST structure pointer [Internationalization for Windows Applications]","_win32_CANDIDATELIST_str","imm/CANDIDATELIST","imm/PCANDIDATELIST","intl.candidatelist","tagCANDIDATELIST"]
old-location: intl\candidatelist.htm
tech.root: Intl
ms.assetid: d60b28fb-0cdd-43b4-8d99-cb829bea6679
ms.date: 08/04/2022
ms.keywords: '*LPCANDIDATELIST, *NPCANDIDATELIST, *PCANDIDATELIST, CANDIDATELIST, CANDIDATELIST structure [Internationalization for Windows Applications], PCANDIDATELIST, PCANDIDATELIST structure pointer [Internationalization for Windows Applications], _win32_CANDIDATELIST_str, imm/CANDIDATELIST, imm/PCANDIDATELIST, intl.candidatelist, tagCANDIDATELIST'
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
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
req.typenames: CANDIDATELIST, *PCANDIDATELIST, *NPCANDIDATELIST, *LPCANDIDATELIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCANDIDATELIST
 - immdev/tagCANDIDATELIST
 - PCANDIDATELIST
 - immdev/PCANDIDATELIST
 - CANDIDATELIST
 - immdev/CANDIDATELIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Imm.h
api_name:
 - CANDIDATELIST
---

# CANDIDATELIST structure


## -description

Contains information about a candidate list.

## -struct-fields

### -field dwSize

Size, in bytes, of the structure, the offset array, and all candidate strings.

### -field dwStyle

Candidate style values. This member can have one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>IME_CAND_UNKNOWN</td>
<td>Candidates are in a style other than listed here.</td>
</tr>
<tr>
<td>IME_CAND_READ</td>
<td>Candidates are in same reading.</td>
</tr>
<tr>
<td>IME_CAND_CODE</td>
<td>Candidates are in a code range.</td>
</tr>
<tr>
<td>IME_CAND_MEANING</td>
<td>Candidates are in same meaning.</td>
</tr>
<tr>
<td>IME_CAND_RADICAL</td>
<td>Candidates use same radical character.</td>
</tr>
<tr>
<td>IME_CAND_STROKES</td>
<td>Candidates are in same number of strokes.</td>
</tr>
</table>
 

For the IME_CAND_CODE style, the candidate list has a special structure depending on the value of the <b>dwCount</b> member. If <b>dwCount</b> is 1, the <b>dwOffset</b> member contains a single DBCS character rather than an offset, and no candidate string is provided. If the <b>dwCount</b> member is greater than 1, the <b>dwOffset</b> member contains valid offsets, and the candidate strings are text representations of individual DBCS character values in hexadecimal notation.

### -field dwCount

Number of candidate strings.

### -field dwSelection

Index of the selected candidate string.

### -field dwPageStart

Index of the first candidate string in the candidate window. This varies as the user presses the PAGE UP and PAGE DOWN keys.

### -field dwPageSize

Number of candidate strings to be shown in one page in the candidate window. The user can move to the next page by pressing IME-defined keys, such as the PAGE UP or PAGE DOWN key. If this number is 0, an application can define a proper value by itself.

### -field dwOffset

Offset to the start of the first candidate string, relative to the start of this structure. The offsets for subsequent strings immediately follow this member, forming an array of 32-bit offsets.

## -remarks

The candidate strings immediately follow the last offset in the <b>dwOffset</b> array.

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-structures">Input Method Manager Structures</a>

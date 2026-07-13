---
UID: NS:imm.tagCANDIDATEFORM
title: CANDIDATEFORM (imm.h)
description: The CANDIDATEFORM (imm.h) structure contains position information for the candidate window. 
helpviewer_keywords: ["*LPCANDIDATEFORM","*NPCANDIDATEFORM","*PCANDIDATEFORM","CANDIDATEFORM","CANDIDATEFORM structure [Internationalization for Windows Applications]","PCANDIDATEFORM","PCANDIDATEFORM structure pointer [Internationalization for Windows Applications]","_win32_CANDIDATEFORM_str","imm/CANDIDATEFORM","imm/PCANDIDATEFORM","intl.candidateform","tagCANDIDATEFORM"]
old-location: intl\candidateform.htm
tech.root: Intl
ms.assetid: 86edcfe0-07f7-4bd7-9444-3a884aeb7926
ms.date: 08/04/2022
ms.keywords: '*LPCANDIDATEFORM, *NPCANDIDATEFORM, *PCANDIDATEFORM, CANDIDATEFORM, CANDIDATEFORM structure [Internationalization for Windows Applications], PCANDIDATEFORM, PCANDIDATEFORM structure pointer [Internationalization for Windows Applications], _win32_CANDIDATEFORM_str, imm/CANDIDATEFORM, imm/PCANDIDATEFORM, intl.candidateform, tagCANDIDATEFORM'
req.header: imm.h
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
req.typenames: CANDIDATEFORM, *PCANDIDATEFORM, *NPCANDIDATEFORM, *LPCANDIDATEFORM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCANDIDATEFORM
 - imm/tagCANDIDATEFORM
 - PCANDIDATEFORM
 - imm/PCANDIDATEFORM
 - CANDIDATEFORM
 - imm/CANDIDATEFORM
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
 - CANDIDATEFORM
---

# CANDIDATEFORM structure


## -description

Contains position information for the candidate window.

## -struct-fields

### -field dwIndex

Candidate list identifier. It is 0 for the first list, 1 for the second, and so on. The maximum index is 3.

### -field dwStyle

Position style. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>CFS_CANDIDATEPOS</td>
<td>Display the upper left corner of the candidate list window at the position specified by <b>ptCurrentPos</b>. The coordinates are relative to the upper left corner of the window containing the list window, and are subject to adjustment by the system.</td>
</tr>
<tr>
<td>CFS_EXCLUDE</td>
<td>Exclude the candidate window from the area specified by <b>rcArea</b>. The <b>ptCurrentPos</b> member specifies the coordinates of the current point of interest, typically the caret position.</td>
</tr>
</table>

### -field ptCurrentPos

A <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure containing the coordinates of the upper left corner of the candidate window or the caret position, depending on the value of <b>dwStyle</b>.

### -field rcArea

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the coordinates of the upper left and lower right corners of the exclusion area.

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-structures">Input Method Manager Structures</a>

---
UID: NS:commctrl.NMCBEENDEDITA
title: NMCBEENDEDITA (commctrl.h)
description: Contains information about the conclusion of an edit operation within a ComboBoxEx control. This structure is used with the CBEN_ENDEDIT notification code. (ANSI)
helpviewer_keywords: ["*LPNMCBEENDEDITA","*PNMCBEENDEDITA","CBENF_DROPDOWN","CBENF_ESCAPE","CBENF_KILLFOCUS","CBENF_RETURN","NMCBEENDEDIT","NMCBEENDEDIT structure [Windows Controls]","NMCBEENDEDITA","NMCBEENDEDITW","PNMCBEENDEDIT","PNMCBEENDEDIT structure pointer [Windows Controls]","_win32_NMCBEENDEDIT","_win32_NMCBEENDEDIT_cpp","commctrl/NMCBEENDEDIT","commctrl/NMCBEENDEDITA","commctrl/NMCBEENDEDITW","commctrl/PNMCBEENDEDIT","controls.NMCBEENDEDIT","controls._win32_NMCBEENDEDIT"]
old-location: controls\NMCBEENDEDIT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboex\structures\nmcbeendedit.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMCBEENDEDITA, *PNMCBEENDEDITA, CBENF_DROPDOWN, CBENF_ESCAPE, CBENF_KILLFOCUS, CBENF_RETURN, NMCBEENDEDIT, NMCBEENDEDIT structure [Windows Controls], NMCBEENDEDITA, NMCBEENDEDITW, PNMCBEENDEDIT, PNMCBEENDEDIT structure pointer [Windows Controls], _win32_NMCBEENDEDIT, _win32_NMCBEENDEDIT_cpp, commctrl/NMCBEENDEDIT, commctrl/NMCBEENDEDITA, commctrl/NMCBEENDEDITW, commctrl/PNMCBEENDEDIT, controls.NMCBEENDEDIT, controls._win32_NMCBEENDEDIT'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMCBEENDEDITW (Unicode) and NMCBEENDEDITA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NMCBEENDEDITA, *LPNMCBEENDEDITA, *PNMCBEENDEDITA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPNMCBEENDEDITA
 - commctrl/LPNMCBEENDEDITA
 - NMCBEENDEDITA
 - commctrl/NMCBEENDEDITA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - NMCBEENDEDIT
 - NMCBEENDEDITA
 - NMCBEENDEDITW
---

# NMCBEENDEDITA structure


## -description

Contains information about the conclusion of an edit operation within a ComboBoxEx control. This structure is used with the <a href="/windows/desktop/Controls/cben-endedit">CBEN_ENDEDIT</a> notification code.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about the notification code.

### -field fChanged

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

A value indicating whether the contents of the control's edit box have changed. This value is nonzero if the contents have been modified, or zero otherwise.

### -field iNewSelection

Type: <b>int</b>

The zero-based index of the item that will be selected after completing the edit operation. This value can be CB_ERR if no item will be selected.

### -field szText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">TCHAR</a></b>

A zero-terminated string that contains the text from within the control's edit box.

### -field iWhy

Type: <b>int</b>

A value that specifies the action that generated the <a href="/windows/desktop/Controls/cben-endedit">CBEN_ENDEDIT</a> notification code. This value can be one of the following: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CBENF_DROPDOWN"></a><a id="cbenf_dropdown"></a><dl>
<dt><b>CBENF_DROPDOWN</b></dt>
</dl>
</td>
<td width="60%">
The user activated the drop-down list.

</td>
</tr>
<tr>
<td width="40%"><a id="CBENF_ESCAPE"></a><a id="cbenf_escape"></a><dl>
<dt><b>CBENF_ESCAPE</b></dt>
</dl>
</td>
<td width="60%">
The user pressed ESC.

</td>
</tr>
<tr>
<td width="40%"><a id="CBENF_KILLFOCUS"></a><a id="cbenf_killfocus"></a><dl>
<dt><b>CBENF_KILLFOCUS</b></dt>
</dl>
</td>
<td width="60%">
The edit box lost the keyboard focus.

</td>
</tr>
<tr>
<td width="40%"><a id="CBENF_RETURN"></a><a id="cbenf_return"></a><dl>
<dt><b>CBENF_RETURN</b></dt>
</dl>
</td>
<td width="60%">
The user completed the edit operation by pressing ENTER.

</td>
</tr>
</table>

## -remarks

> [!NOTE]
> The commctrl.h header defines NMCBEENDEDIT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).


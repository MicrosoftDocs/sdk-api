---
UID: NC:richedit.EDITWORDBREAKPROCEX
title: EDITWORDBREAKPROCEX (richedit.h)
description: The EditWordBreakProcEx function is an application defined callback function used with the EM_SETWORDBREAKPROCEX message.
helpviewer_keywords: ["EditWordBreakProcEx","EditWordBreakProcEx callback","EditWordBreakProcEx callback function [Windows Controls]","_win32_EditWordBreakProcEx","_win32_EditWordBreakProcEx_cpp","controls.EditWordBreakProcEx","controls._win32_EditWordBreakProcEx","richedit/EditWordBreakProcEx"]
old-location: controls\EditWordBreakProcEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditcallbackfunctions\editwordbreakprocex.htm
ms.date: 12/05/2018
ms.keywords: EditWordBreakProcEx, EditWordBreakProcEx callback, EditWordBreakProcEx callback function [Windows Controls], _win32_EditWordBreakProcEx, _win32_EditWordBreakProcEx_cpp, controls.EditWordBreakProcEx, controls._win32_EditWordBreakProcEx, richedit/EditWordBreakProcEx
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EDITWORDBREAKPROCEX
 - richedit/EDITWORDBREAKPROCEX
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
 - EditWordBreakProcEx
---

# EDITWORDBREAKPROCEX callback function


## -description

The <i>EditWordBreakProcEx</i> function is an application defined  callback function used with the <a href="/windows/win32/controls/em-setwordbreakprocex">EM_SETWORDBREAKPROCEX</a> message. It determines the character index of the word break or the character class and word-break flags of the characters in the specified text. The 
			<b>EDITWORDBREAKPROCEX</b> type defines a pointer to this callback function. <i>EditWordBreakProcEx</i> is a placeholder for the application-defined function name.

## -parameters

### -param pchText [in]

Type: <b>char*</b>

Pointer to the text at the current position. If 
					<i>code</i> specifies movement to the left, the text is in the elements 
					<i>pchText</i> 
					[–1] through 
					<i>pchText</i> [-<i>cchText</i>], and 
					<i>pchText</i>[0] is undefined. For all other actions, the text is in the elements 
					<i>pchText</i>[0] through 
					<i>pchText</i>[
					<i>cchText</i>–1].

### -param cchText [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Number of characters in the buffer in the direction specified by 
					<i>code</i>.

### -param bCharSet [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Character set of the text.

### -param action

#### - code [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">INT</a></b>

Word break action. Can be one of the values described for the 
					<i>code</i> parameter in the <a href="/windows/win32/controls/em-findwordbreak">EM_FINDWORDBREAK</a> message.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

The function returns a value based on the 
						<i>code</i> parameter.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>code parameter</b></dt>
</dl>
</td>
<td width="60%">
Return value

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WB_CLASSIFY</b></dt>
</dl>
</td>
<td width="60%">
Returns the character class and word-break flags of the character at the specified position.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WB_ISDELIMITER</b></dt>
</dl>
</td>
<td width="60%">
Returns <b>TRUE</b> if the character at the specified position is a delimiter or <b>FALSE</b> if the character is not.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>All other values</b></dt>
</dl>
</td>
<td width="60%">
Returns the character index of the word break.

</td>
</tr>
</table>

## -remarks

An application must install the callback function by specifying the address of the callback function in an <a href="/windows/win32/controls/em-setwordbreakprocex">EM_SETWORDBREAKPROCEX</a> message. 

For Microsoft Rich Edit 2.0 and later, Rich Edit no longer supports <i>EditWordBreakProcEx</i>. Users can send 
				<a href="/windows/win32/controls/em-setwordbreakproc">EM_SETWORDBREAKPROC</a> to set <a href="/windows/win32/api/winuser/nc-winuser-editwordbreakproca">EditWordBreakProc</a>, which is now enhanced to support the passing of Unicode text.

## -see-also

<a href="/windows/win32/controls/em-findwordbreak">EM_FINDWORDBREAK</a>



<a href="/windows/win32/controls/em-setwordbreakprocex">EM_SETWORDBREAKPROCEX</a>



<a href="/windows/win32/api/winuser/nc-winuser-editwordbreakproca">EditWordBreakProc</a>



<b>Reference</b>

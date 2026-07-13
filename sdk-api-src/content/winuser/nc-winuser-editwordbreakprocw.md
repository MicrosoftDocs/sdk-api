---
UID: NC:winuser.EDITWORDBREAKPROCW
title: EDITWORDBREAKPROCW (winuser.h)
description: An application-defined callback function used with the EM_SETWORDBREAKPROC message. (Unicode)
helpviewer_keywords: ["EDITWORDBREAKPROCA","EDITWORDBREAKPROCW","EditWordBreakProc","EditWordBreakProc callback","EditWordBreakProc callback function [Windows Controls]","WB_CLASSIFY","WB_ISDELIMITER","WB_LEFT","WB_LEFTBREAK","WB_MOVEWORDLEFT","WB_MOVEWORDRIGHT","WB_RIGHT","WB_RIGHTBREAK","_win32_EditWordBreakProc","_win32_EditWordBreakProc_cpp","controls.EditWordBreakProc","controls._win32_EditWordBreakProc","winuser/EDITWORDBREAKPROCA","winuser/EDITWORDBREAKPROCW","winuser/EditWordBreakProc"]
old-location: controls\EditWordBreakProc.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolfunctions\editwordbreakproc.htm
ms.date: 12/05/2018
ms.keywords: EDITWORDBREAKPROCA, EDITWORDBREAKPROCW, EditWordBreakProc, EditWordBreakProc callback, EditWordBreakProc callback function [Windows Controls], WB_CLASSIFY, WB_ISDELIMITER, WB_LEFT, WB_LEFTBREAK, WB_MOVEWORDLEFT, WB_MOVEWORDRIGHT, WB_RIGHT, WB_RIGHTBREAK, _win32_EditWordBreakProc, _win32_EditWordBreakProc_cpp, controls.EditWordBreakProc, controls._win32_EditWordBreakProc, winuser/EDITWORDBREAKPROCA, winuser/EDITWORDBREAKPROCW, winuser/EditWordBreakProc
req.header: winuser.h
req.include-header: Windows.h
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
 - EDITWORDBREAKPROCW
 - winuser/EDITWORDBREAKPROCW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winuser.h
api_name:
 - EditWordBreakProc
 - EDITWORDBREAKPROCA
 - EDITWORDBREAKPROCW
---

# EDITWORDBREAKPROCW callback function


## -description

An application-defined callback function used with the <a href="/windows/desktop/Controls/em-setwordbreakproc">EM_SETWORDBREAKPROC</a> message. A multiline edit control or a rich edit control calls an <i>EditWordBreakProc</i> function to break a line of text.

The <b>EDITWORDBREAKPROC</b> type defines a pointer to this callback function. <i>EditWordBreakProc</i> is a placeholder for the application-defined function name.

## -parameters

### -param lpch [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a></b>

A pointer to the text of the edit control.

### -param ichCurrent [in]

Type: <b>int</b>

An index to a character position in the buffer of text that identifies the point at which the function should begin checking for a word break.

### -param cch [in]

Type: <b>int</b>

The number of <b>TCHARs</b> in the edit control text. For the ANSI text, this is the number of bytes; for the Unicode text, this is the number of WCHARs.

### -param code [in]

Type: <b>int</b>

The action to be taken by the callback function. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WB_CLASSIFY"></a><a id="wb_classify"></a><dl>
<dt><b>WB_CLASSIFY</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the character class and word break flags of the character at the specified position. This value is for use with rich edit controls.

</td>
</tr>
<tr>
<td width="40%"><a id="WB_ISDELIMITER"></a><a id="wb_isdelimiter"></a><dl>
<dt><b>WB_ISDELIMITER</b></dt>
</dl>
</td>
<td width="60%">
Checks whether the character at the specified position is a delimiter.

</td>
</tr>
<tr>
<td width="40%"><a id="WB_LEFT"></a><a id="wb_left"></a><dl>
<dt><b>WB_LEFT</b></dt>
</dl>
</td>
<td width="60%">
Finds the beginning of a word to the left of the specified position.

</td>
</tr>
<tr>
<td width="40%"><a id="WB_LEFTBREAK"></a><a id="wb_leftbreak"></a><dl>
<dt><b>WB_LEFTBREAK</b></dt>
</dl>
</td>
<td width="60%">
Finds the end-of-word delimiter to the left of the specified position. This value is for use with rich edit controls.

</td>
</tr>
<tr>
<td width="40%"><a id="WB_MOVEWORDLEFT"></a><a id="wb_movewordleft"></a><dl>
<dt><b>WB_MOVEWORDLEFT</b></dt>
</dl>
</td>
<td width="60%">
Finds the beginning of a word to the left of the specified position. This value is used during CTRL+LEFT key processing. This value is for use with rich edit controls.

</td>
</tr>
<tr>
<td width="40%"><a id="WB_MOVEWORDRIGHT"></a><a id="wb_movewordright"></a><dl>
<dt><b>WB_MOVEWORDRIGHT</b></dt>
</dl>
</td>
<td width="60%">
Finds the beginning of a word to the right of the specified position. This value is used during CTRL+RIGHT key processing. This value is for use with rich edit controls.

</td>
</tr>
<tr>
<td width="40%"><a id="WB_RIGHT"></a><a id="wb_right"></a><dl>
<dt><b>WB_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Finds the beginning of a word to the right of the specified position. This is useful in right-aligned edit controls.

</td>
</tr>
<tr>
<td width="40%"><a id="WB_RIGHTBREAK"></a><a id="wb_rightbreak"></a><dl>
<dt><b>WB_RIGHTBREAK</b></dt>
</dl>
</td>
<td width="60%">
Finds the end-of-word delimiter to the right of the specified position. This is useful in right-aligned edit controls. This value is for use with rich edit controls.

</td>
</tr>
</table>

## -returns

Type: <b>int</b>

If the 
						<i>code</i> parameter specifies <b>WB_ISDELIMITER</b>, the return value is nonzero (TRUE) if the character at the specified position is a delimiter, or zero if it is not. If the 
						<i>code</i> parameter specifies <b>WB_CLASSIFY</b>, the return value is the character class and word break flags of the character at the specified position. Otherwise, the return value is an index to the beginning of a word in the buffer of text.

## -remarks

A carriage return followed by a line feed must be treated as a single word by the callback function. Two carriage returns followed by a line feed also must be treated as a single word. 

An application must install the callback function by specifying the address of the callback function in an <a href="/windows/desktop/Controls/em-setwordbreakproc">EM_SETWORDBREAKPROC</a> message. 

<b>Rich Edit 1.0:</b>Microsoft Rich Edit 1.0 only passes back ANSI characters to <i>EditWordBreakProc</i>. For rich edit controls, you can alternately use the <a href="/windows/desktop/Controls/em-setwordbreakprocex">EM_SETWORDBREAKPROCEX</a> message to replace the default extended word break procedure with an <a href="/windows/desktop/api/richedit/nc-richedit-editwordbreakprocex">EditWordBreakProcEx</a> callback function. This function provides additional information about the text, such as the character set. 

<b>Rich Edit 2.0 and later:</b>Microsoft Rich Edit 2.0 and later only pass back Unicode characters to <i>EditWordBreakProc</i>. Thus, an ANSI application would convert the Rich Edit-supplied Unicode string using <a href="/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte">WideCharToMultiByte</a>, and then translate the indices appropriately. 





> [!NOTE]
> The winuser.h header defines EDITWORDBREAKPROC as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Controls/em-findwordbreak">EM_FINDWORDBREAK</a>



<a href="/windows/desktop/Controls/em-setwordbreakproc">EM_SETWORDBREAKPROC</a>



<a href="/windows/desktop/Controls/em-setwordbreakprocex">EM_SETWORDBREAKPROCEX</a>



<a href="/windows/desktop/api/richedit/nc-richedit-editwordbreakprocex">EditWordBreakProcEx</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a>

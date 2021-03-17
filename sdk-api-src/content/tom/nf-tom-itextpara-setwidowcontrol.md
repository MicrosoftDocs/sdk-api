---
UID: NF:tom.ITextPara.SetWidowControl
title: ITextPara::SetWidowControl (tom.h)
description: Controls the suppression of widows and orphans.
helpviewer_keywords: ["ITextPara interface [Windows Controls]","SetWidowControl method","ITextPara.SetWidowControl","ITextPara::SetWidowControl","SetWidowControl","SetWidowControl method [Windows Controls]","SetWidowControl method [Windows Controls]","ITextPara interface","_win32_ITextPara_SetWidowControl","_win32_ITextPara_SetWidowControl_cpp","controls.ITextPara_SetWidowControl","controls._win32_ITextPara_SetWidowControl","tom/ITextPara::SetWidowControl"]
old-location: controls\ITextPara_SetWidowControl.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setwidowcontrol.htm
ms.date: 12/05/2018
ms.keywords: ITextPara interface [Windows Controls],SetWidowControl method, ITextPara.SetWidowControl, ITextPara::SetWidowControl, SetWidowControl, SetWidowControl method [Windows Controls], SetWidowControl method [Windows Controls],ITextPara interface, _win32_ITextPara_SetWidowControl, _win32_ITextPara_SetWidowControl_cpp, controls.ITextPara_SetWidowControl, controls._win32_ITextPara_SetWidowControl, tom/ITextPara::SetWidowControl
req.header: tom.h
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
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextPara::SetWidowControl
 - tom/ITextPara::SetWidowControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextPara.SetWidowControl
---

# ITextPara::SetWidowControl


## -description

Controls the suppression of widows and orphans.

## -parameters

### -param Value [in]

Type: <b>long</b>

A tomBool value that controls the suppression of widows and orphans. It can be one of the following possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>tomTrue</dt>
</dl>
</td>
<td width="60%">
Prevents printing of widows and orphans.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>tomFalse</dt>
</dl>
</td>
<td width="60%">
Allows printing of widows and orphans.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>tomToggle</dt>
</dl>
</td>
<td width="60%">
The value is toggled.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>tomUndefined</dt>
</dl>
</td>
<td width="60%">
No change.

</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::SetWidowControl</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Value</b></dt>
</dl>
</td>
<td width="60%">
Meaning

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Write access is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The paragraph formatting object is attached to a range that has been deleted.

</td>
</tr>
</table>

## -remarks

This method is included for compatibility with Microsoft Word; it does not affect how the rich edit control displays text.

A widow is created when the last line of a paragraph is printed by itself at the top of a page. An orphan is when the first line of a paragraph is printed by itself at the bottom of a page.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
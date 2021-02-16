---
UID: NF:tom.ITextPara.GetWidowControl
title: ITextPara::GetWidowControl (tom.h)
description: Retrieves the widow and orphan control state for the paragraphs in a range.
helpviewer_keywords: ["GetWidowControl","GetWidowControl method [Windows Controls]","GetWidowControl method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","GetWidowControl method","ITextPara.GetWidowControl","ITextPara::GetWidowControl","_win32_ITextPara_GetWidowControl","_win32_ITextPara_GetWidowControl_cpp","controls.ITextPara_GetWidowControl","controls._win32_ITextPara_GetWidowControl","tom/ITextPara::GetWidowControl"]
old-location: controls\ITextPara_GetWidowControl.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getwidowcontrol.htm
ms.date: 12/05/2018
ms.keywords: GetWidowControl, GetWidowControl method [Windows Controls], GetWidowControl method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetWidowControl method, ITextPara.GetWidowControl, ITextPara::GetWidowControl, _win32_ITextPara_GetWidowControl, _win32_ITextPara_GetWidowControl_cpp, controls.ITextPara_GetWidowControl, controls._win32_ITextPara_GetWidowControl, tom/ITextPara::GetWidowControl
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
 - ITextPara::GetWidowControl
 - tom/ITextPara::GetWidowControl
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
 - ITextPara.GetWidowControl
---

# ITextPara::GetWidowControl


## -description

Retrieves the widow and orphan control state for the paragraphs in a range.

## -parameters

### -param pValue

Type: <b>long*</b>

A <a href="/windows/desktop/Controls/about-text-object-model">tomBool</a> value that indicates the state of widow and orphan control. It can be one of the following values. 
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomTrue</b></td>
<td>Prevents the printing of a widow or orphan</td>
</tr>
<tr>
<td><b>tomFalse</b></td>
<td>Allows the printing of a widow or orphan.</td>
</tr>
<tr>
<td><b>tomUndefined</b></td>
<td>The widow-control property is undefined.</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::GetWidowControl</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The paragraph formatting object is attached to a range that has been deleted.

</td>
</tr>
</table>

## -remarks

A widow is created when the last line of a paragraph is printed by itself at the top of a page. An orphan is when the first line of a paragraph is printed by itself at the bottom of a page.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setwidowcontrol">SetWidowControl</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
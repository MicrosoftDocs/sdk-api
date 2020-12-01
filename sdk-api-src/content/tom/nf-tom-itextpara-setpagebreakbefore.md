---
UID: NF:tom.ITextPara.SetPageBreakBefore
title: ITextPara::SetPageBreakBefore (tom.h)
description: Controls whether there is a page break before each paragraph in a range.
helpviewer_keywords: ["ITextPara interface [Windows Controls]","SetPageBreakBefore method","ITextPara.SetPageBreakBefore","ITextPara::SetPageBreakBefore","SetPageBreakBefore","SetPageBreakBefore method [Windows Controls]","SetPageBreakBefore method [Windows Controls]","ITextPara interface","_win32_ITextPara_SetPageBreakBefore","_win32_ITextPara_SetPageBreakBefore_cpp","controls.ITextPara_SetPageBreakBefore","controls._win32_ITextPara_SetPageBreakBefore","tom/ITextPara::SetPageBreakBefore"]
old-location: controls\ITextPara_SetPageBreakBefore.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setpagebreakbefore.htm
ms.date: 12/05/2018
ms.keywords: ITextPara interface [Windows Controls],SetPageBreakBefore method, ITextPara.SetPageBreakBefore, ITextPara::SetPageBreakBefore, SetPageBreakBefore, SetPageBreakBefore method [Windows Controls], SetPageBreakBefore method [Windows Controls],ITextPara interface, _win32_ITextPara_SetPageBreakBefore, _win32_ITextPara_SetPageBreakBefore_cpp, controls.ITextPara_SetPageBreakBefore, controls._win32_ITextPara_SetPageBreakBefore, tom/ITextPara::SetPageBreakBefore
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
 - ITextPara::SetPageBreakBefore
 - tom/ITextPara::SetPageBreakBefore
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
 - ITextPara.SetPageBreakBefore
---

# ITextPara::SetPageBreakBefore


## -description

Controls whether there is a page break before each paragraph in a range.

## -parameters

### -param Value [in]

Type: <b>long</b>

A <a href="/windows/desktop/Controls/about-text-object-model">tomBool</a> value that controls page breaks before paragraphs. It can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>tomTrue</b></dt>
</dl>
</td>
<td width="60%">
Paragraphs in this range must begin on a new page.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>tomFalse</b></dt>
</dl>
</td>
<td width="60%">
Paragraphs in this range do not need to begin on a new page.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>tomToggle</b></dt>
</dl>
</td>
<td width="60%">
Toggle the property value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>tomUndefined</b></dt>
</dl>
</td>
<td width="60%">
The property is undefined.

</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::SetPageBreakBefore</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
---
UID: NF:tom.ITextPara.GetPageBreakBefore
title: ITextPara::GetPageBreakBefore (tom.h)
description: Determines whether each paragraph in the range must begin on a new page.
helpviewer_keywords: ["GetPageBreakBefore","GetPageBreakBefore method [Windows Controls]","GetPageBreakBefore method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","GetPageBreakBefore method","ITextPara.GetPageBreakBefore","ITextPara::GetPageBreakBefore","_win32_ITextPara_GetPageBreakBefore","_win32_ITextPara_GetPageBreakBefore_cpp","controls.ITextPara_GetPageBreakBefore","controls._win32_ITextPara_GetPageBreakBefore","tom/ITextPara::GetPageBreakBefore"]
old-location: controls\ITextPara_GetPageBreakBefore.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getpagebreakbefore.htm
ms.date: 12/05/2018
ms.keywords: GetPageBreakBefore, GetPageBreakBefore method [Windows Controls], GetPageBreakBefore method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetPageBreakBefore method, ITextPara.GetPageBreakBefore, ITextPara::GetPageBreakBefore, _win32_ITextPara_GetPageBreakBefore, _win32_ITextPara_GetPageBreakBefore_cpp, controls.ITextPara_GetPageBreakBefore, controls._win32_ITextPara_GetPageBreakBefore, tom/ITextPara::GetPageBreakBefore
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
 - ITextPara::GetPageBreakBefore
 - tom/ITextPara::GetPageBreakBefore
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
 - ITextPara.GetPageBreakBefore
---

# ITextPara::GetPageBreakBefore


## -description

Determines whether each paragraph in the range must begin on a new page.

## -parameters

### -param pValue

Type: <b>long*</b>

A variable that is one of the following values: 
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>tomTrue</td>
<td>Each paragraph in this range must begin on a new page.</td>
</tr>
<tr>
<td>tomFalse</td>
<td>The paragraphs in this range do not need to begin on a new page.</td>
</tr>
<tr>
<td>tomUndefined</td>
<td>The property is undefined.</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::GetPageBreakBefore</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setpagebreakbefore">SetPageBreakBefore</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
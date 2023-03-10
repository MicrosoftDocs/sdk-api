---
UID: NF:tom.ITextPara.GetListAlignment
title: ITextPara::GetListAlignment (tom.h)
description: Retrieves the kind of alignment to use for bulleted and numbered lists.
helpviewer_keywords: ["GetListAlignment","GetListAlignment method [Windows Controls]","GetListAlignment method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","GetListAlignment method","ITextPara.GetListAlignment","ITextPara::GetListAlignment","_win32_ITextPara_GetListAlignment","_win32_ITextPara_GetListAlignment_cpp","controls.ITextPara_GetListAlignment","controls._win32_ITextPara_GetListAlignment","tom/ITextPara::GetListAlignment"]
old-location: controls\ITextPara_GetListAlignment.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getlistalignment.htm
ms.date: 12/05/2018
ms.keywords: GetListAlignment, GetListAlignment method [Windows Controls], GetListAlignment method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetListAlignment method, ITextPara.GetListAlignment, ITextPara::GetListAlignment, _win32_ITextPara_GetListAlignment, _win32_ITextPara_GetListAlignment_cpp, controls.ITextPara_GetListAlignment, controls._win32_ITextPara_GetListAlignment, tom/ITextPara::GetListAlignment
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
 - ITextPara::GetListAlignment
 - tom/ITextPara::GetListAlignment
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
 - ITextPara.GetListAlignment
---

# ITextPara::GetListAlignment


## -description

Retrieves the kind of alignment to use for bulleted and numbered lists.

## -parameters

### -param pValue

Type: <b>long*</b>

A variable that is one of the following values to indicate the kind of bullet and numbering alignment. 
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>tomAlignLeft</td>
<td>Text is left aligned.</td>
</tr>
<tr>
<td>tomAlignCenter</td>
<td>Text is centered in the line.</td>
</tr>
<tr>
<td>tomAlignRight</td>
<td>Text is right aligned.</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::GetListAlignment</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

For a description of the different types of lists, see the <a href="/windows/desktop/api/tom/nf-tom-itextpara-getlisttype">ITextPara::GetListType</a> method.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getlisttype">GetListType</a>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setlistalignment">SetListAlignment</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
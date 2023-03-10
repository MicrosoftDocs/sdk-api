---
UID: NF:tom.ITextPara.GetListStart
title: ITextPara::GetListStart (tom.h)
description: Retrieves the starting value or code of a list numbering sequence.
helpviewer_keywords: ["GetListStart","GetListStart method [Windows Controls]","GetListStart method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","GetListStart method","ITextPara.GetListStart","ITextPara::GetListStart","_win32_ITextPara_GetListStart","_win32_ITextPara_GetListStart_cpp","controls.ITextPara_GetListStart","controls._win32_ITextPara_GetListStart","tom/ITextPara::GetListStart"]
old-location: controls\ITextPara_GetListStart.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getliststart.htm
ms.date: 12/05/2018
ms.keywords: GetListStart, GetListStart method [Windows Controls], GetListStart method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetListStart method, ITextPara.GetListStart, ITextPara::GetListStart, _win32_ITextPara_GetListStart, _win32_ITextPara_GetListStart_cpp, controls.ITextPara_GetListStart, controls._win32_ITextPara_GetListStart, tom/ITextPara::GetListStart
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
 - ITextPara::GetListStart
 - tom/ITextPara::GetListStart
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
 - ITextPara.GetListStart
---

# ITextPara::GetListStart


## -description

Retrieves the starting value or code of a list numbering sequence.

## -parameters

### -param pValue

Type: <b>long*</b>

The starting value or code of a list numbering sequence. For the possible values, see the <a href="/windows/desktop/api/tom/nf-tom-itextpara-getlisttype">ITextPara::GetListType</a> method.

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::GetListStart</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

For a discussion on which sequence to use, see the <a href="/windows/desktop/api/tom/nf-tom-itextpara-getlisttype">ITextPara::GetListType</a> method.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getlisttype">GetListType</a>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setliststart">SetListStart</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setlisttype">SetListType</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
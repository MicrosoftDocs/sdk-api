---
UID: NF:tom.ITextPara.SetKeepTogether
title: ITextPara::SetKeepTogether (tom.h)
description: Controls whether page breaks are allowed within a paragraph in a range.
helpviewer_keywords: ["ITextPara interface [Windows Controls]","SetKeepTogether method","ITextPara.SetKeepTogether","ITextPara::SetKeepTogether","SetKeepTogether","SetKeepTogether method [Windows Controls]","SetKeepTogether method [Windows Controls]","ITextPara interface","_win32_ITextPara_SetKeepTogether","_win32_ITextPara_SetKeepTogether_cpp","controls.ITextPara_SetKeepTogether","controls._win32_ITextPara_SetKeepTogether","tom/ITextPara::SetKeepTogether"]
old-location: controls\ITextPara_SetKeepTogether.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setkeeptogether.htm
ms.date: 12/05/2018
ms.keywords: ITextPara interface [Windows Controls],SetKeepTogether method, ITextPara.SetKeepTogether, ITextPara::SetKeepTogether, SetKeepTogether, SetKeepTogether method [Windows Controls], SetKeepTogether method [Windows Controls],ITextPara interface, _win32_ITextPara_SetKeepTogether, _win32_ITextPara_SetKeepTogether_cpp, controls.ITextPara_SetKeepTogether, controls._win32_ITextPara_SetKeepTogether, tom/ITextPara::SetKeepTogether
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
 - ITextPara::SetKeepTogether
 - tom/ITextPara::SetKeepTogether
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
 - ITextPara.SetKeepTogether
---

# ITextPara::SetKeepTogether


## -description

Controls whether page breaks are allowed within a paragraph in a range.

## -parameters

### -param Value [in]

Type: <b>long</b>

Indicates whether page breaks are allowed within a paragraph in a range. It can be one of the following possible values. 

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
Page breaks are not allowed within a paragraph.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>tomFalse</dt>
</dl>
</td>
<td width="60%">
Page breaks are allowed within a paragraph.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>tomUndefined</dt>
</dl>
</td>
<td width="60%">
The property is undefined.

</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::SetKeepTogether</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

This property corresponds to the PFE_KEEP effect described in the <a href="/windows/desktop/api/richedit/ns-richedit-paraformat2">PARAFORMAT2</a> structure.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<a href="/windows/desktop/api/richedit/ns-richedit-paraformat2">PARAFORMAT2</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
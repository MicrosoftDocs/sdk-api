---
UID: NF:tom.ITextPara.SetNoLineNumber
title: ITextPara::SetNoLineNumber (tom.h)
description: Determines whether to suppress line numbering of paragraphs in a range.
helpviewer_keywords: ["ITextPara interface [Windows Controls]","SetNoLineNumber method","ITextPara.SetNoLineNumber","ITextPara::SetNoLineNumber","SetNoLineNumber","SetNoLineNumber method [Windows Controls]","SetNoLineNumber method [Windows Controls]","ITextPara interface","_win32_ITextPara_SetNoLineNumber","_win32_ITextPara_SetNoLineNumber_cpp","controls.ITextPara_SetNoLineNumber","controls._win32_ITextPara_SetNoLineNumber","tom/ITextPara::SetNoLineNumber"]
old-location: controls\ITextPara_SetNoLineNumber.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setnolinenumber.htm
ms.date: 12/05/2018
ms.keywords: ITextPara interface [Windows Controls],SetNoLineNumber method, ITextPara.SetNoLineNumber, ITextPara::SetNoLineNumber, SetNoLineNumber, SetNoLineNumber method [Windows Controls], SetNoLineNumber method [Windows Controls],ITextPara interface, _win32_ITextPara_SetNoLineNumber, _win32_ITextPara_SetNoLineNumber_cpp, controls.ITextPara_SetNoLineNumber, controls._win32_ITextPara_SetNoLineNumber, tom/ITextPara::SetNoLineNumber
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
 - ITextPara::SetNoLineNumber
 - tom/ITextPara::SetNoLineNumber
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
 - ITextPara.SetNoLineNumber
---

# ITextPara::SetNoLineNumber


## -description

Determines whether to suppress line numbering of paragraphs in a range.

## -parameters

### -param Value [in]

Type: <b>long</b>

Indicates if line numbering is suppressed. It can be one of the following possible values.

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
Line numbering is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>tomFalse</dt>
</dl>
</td>
<td width="60%">
Line numbering is enabled.

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

If <b>ITextPara::SetNoLineNumber</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

This property concerns the numbering of paragraphs in a range. If 
				<i>Value</i> is <b>tomFalse</b>, the number of the paragraph appears on the first line of the paragraph.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
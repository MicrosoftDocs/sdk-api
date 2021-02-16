---
UID: NF:tom.ITextPara.SetIndents
title: ITextPara::SetIndents (tom.h)
description: Sets the first-line indent, the left indent, and the right indent for a paragraph.
helpviewer_keywords: ["ITextPara interface [Windows Controls]","SetIndents method","ITextPara.SetIndents","ITextPara::SetIndents","SetIndents","SetIndents method [Windows Controls]","SetIndents method [Windows Controls]","ITextPara interface","_win32_ITextPara_SetIndents","_win32_ITextPara_SetIndents_cpp","controls.ITextPara_SetIndents","controls._win32_ITextPara_SetIndents","tom/ITextPara::SetIndents"]
old-location: controls\ITextPara_SetIndents.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setindents.htm
ms.date: 12/05/2018
ms.keywords: ITextPara interface [Windows Controls],SetIndents method, ITextPara.SetIndents, ITextPara::SetIndents, SetIndents, SetIndents method [Windows Controls], SetIndents method [Windows Controls],ITextPara interface, _win32_ITextPara_SetIndents, _win32_ITextPara_SetIndents_cpp, controls.ITextPara_SetIndents, controls._win32_ITextPara_SetIndents, tom/ITextPara::SetIndents
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
 - ITextPara::SetIndents
 - tom/ITextPara::SetIndents
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
 - ITextPara.SetIndents
---

# ITextPara::SetIndents


## -description

Sets the first-line indent, the left indent, and the right indent for a paragraph.

## -parameters

### -param First [in]

Type: <b>float</b>

Indent of the first line in a paragraph, relative to the left indent. The value is in floating-point points and can be positive or negative.

### -param Left [in]

Type: <b>float</b>

Left indent of all lines except the first line in a paragraph, relative to left margin. The value is in floating-point points and can be positive or negative.

### -param Right [in]

Type: <b>float</b>

Right indent of all lines in paragraph, relative to the right margin. The value is in floating-point points and can be positive or negative. This value is optional.

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::SetIndents</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

Line indents are not allowed to position text in the margins. If the first-line indent is set to a negative value (for an outdented paragraph) while the left indent is zero, the first-line indent is reset to zero. To avoid this problem while retaining property sets, set the first-line indent value equal to zero either explicitly or by calling the <a href="/windows/desktop/api/tom/nf-tom-itextpara-reset">ITextPara::Reset</a> method. Then, call <b>ITextPara::SetIndents</b> to set a nonnegative, left-indent value and set the desired first-line indent.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-reset">Reset</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
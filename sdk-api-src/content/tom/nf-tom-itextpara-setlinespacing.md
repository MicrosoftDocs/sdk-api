---
UID: NF:tom.ITextPara.SetLineSpacing
title: ITextPara::SetLineSpacing (tom.h)
description: Sets the paragraph line-spacing rule and the line spacing for a paragraph.
helpviewer_keywords: ["ITextPara interface [Windows Controls]","SetLineSpacing method","ITextPara.SetLineSpacing","ITextPara::SetLineSpacing","SetLineSpacing","SetLineSpacing method [Windows Controls]","SetLineSpacing method [Windows Controls]","ITextPara interface","_win32_ITextPara_SetLineSpacing","_win32_ITextPara_SetLineSpacing_cpp","controls.ITextPara_SetLineSpacing","controls._win32_ITextPara_SetLineSpacing","tom/ITextPara::SetLineSpacing"]
old-location: controls\ITextPara_SetLineSpacing.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setlinespacing.htm
ms.date: 12/05/2018
ms.keywords: ITextPara interface [Windows Controls],SetLineSpacing method, ITextPara.SetLineSpacing, ITextPara::SetLineSpacing, SetLineSpacing, SetLineSpacing method [Windows Controls], SetLineSpacing method [Windows Controls],ITextPara interface, _win32_ITextPara_SetLineSpacing, _win32_ITextPara_SetLineSpacing_cpp, controls.ITextPara_SetLineSpacing, controls._win32_ITextPara_SetLineSpacing, tom/ITextPara::SetLineSpacing
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
 - ITextPara::SetLineSpacing
 - tom/ITextPara::SetLineSpacing
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
 - ITextPara.SetLineSpacing
---

# ITextPara::SetLineSpacing


## -description

Sets the paragraph line-spacing rule and the line spacing for a paragraph.

## -parameters

### -param Rule [in]

Type: <b>long</b>

Value of new line-spacing rule. For a list of possible rule values and further discussion, see the <a href="/windows/desktop/api/tom/nf-tom-itextpara-getlinespacingrule">ITextPara::GetLineSpacingRule</a> method.

### -param Spacing [in]

Type: <b>float</b>

Value of new line spacing. If the line-spacing rule treats the <i>Spacing</i> value as a linear dimension, then <i>Spacing</i> is given in floating-point points.

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::SetLineSpacing</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

The line-spacing rule and line spacing work together, and as a result, they must be set together, much as the first and left indents need to be set together.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getlinespacingrule">GetLineSpacingRule</a>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
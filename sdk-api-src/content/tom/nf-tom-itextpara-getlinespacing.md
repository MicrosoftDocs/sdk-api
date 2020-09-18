---
UID: NF:tom.ITextPara.GetLineSpacing
title: ITextPara::GetLineSpacing (tom.h)
description: Retrieves the line-spacing value for the text range.
helpviewer_keywords: ["GetLineSpacing","GetLineSpacing method [Windows Controls]","GetLineSpacing method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","GetLineSpacing method","ITextPara.GetLineSpacing","ITextPara::GetLineSpacing","_win32_ITextPara_GetLineSpacing","_win32_ITextPara_GetLineSpacing_cpp","controls.ITextPara_GetLineSpacing","controls._win32_ITextPara_GetLineSpacing","tom/ITextPara::GetLineSpacing"]
old-location: controls\ITextPara_GetLineSpacing.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getlinespacing.htm
ms.date: 12/05/2018
ms.keywords: GetLineSpacing, GetLineSpacing method [Windows Controls], GetLineSpacing method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetLineSpacing method, ITextPara.GetLineSpacing, ITextPara::GetLineSpacing, _win32_ITextPara_GetLineSpacing, _win32_ITextPara_GetLineSpacing_cpp, controls.ITextPara_GetLineSpacing, controls._win32_ITextPara_GetLineSpacing, tom/ITextPara::GetLineSpacing
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
 - ITextPara::GetLineSpacing
 - tom/ITextPara::GetLineSpacing
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
 - ITextPara.GetLineSpacing
---

# ITextPara::GetLineSpacing


## -description

Retrieves the line-spacing value for the text range.

## -parameters

### -param pValue

Type: <b>float*</b>

The line-spacing value. The following table shows how this value is interpreted for the different line-spacing rules. 
					

<table class="clsStd">
<tr>
<th>Line spacing rule</th>
<th>Meaning</th>
</tr>
<tr>
<td>tomLineSpaceSingle</td>
<td>The line-spacing value is ignored. </td>
</tr>
<tr>
<td>tomLineSpace1pt5</td>
<td>The line-spacing value is ignored. </td>
</tr>
<tr>
<td>tomLineSpaceDouble</td>
<td>The line-spacing value is ignored. </td>
</tr>
<tr>
<td>tomLineSpaceAtLeast</td>
<td>The line-spacing value specifies the spacing, in floating-point points, from one line to the next. However, if the value is less than single spacing, the control displays single-spaced text.</td>
</tr>
<tr>
<td>tomLineSpaceExactly</td>
<td>The line-spacing value specifies the exact spacing, in floating-point points, from one line to the next (even if the value is less than single spacing).</td>
</tr>
<tr>
<td>tomLineSpaceMultiple</td>
<td>The line-spacing value specifies the line spacing, in lines.</td>
</tr>
</table>

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::GetLineSpacing</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

To retrieve the line-spacing rule, call the <a href="/windows/desktop/api/tom/nf-tom-itextpara-getlinespacingrule">ITextPara::GetLineSpacingRule</a> method.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getlinespacingrule">GetLineSpacingRule</a>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setlinespacing">SetLineSpacing</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
---
UID: NF:tom.ITextPara.GetLeftIndent
title: ITextPara::GetLeftIndent (tom.h)
description: Retrieves the distance used to indent all lines except the first line of a paragraph. The distance is relative to the left margin.
helpviewer_keywords: ["GetLeftIndent","GetLeftIndent method [Windows Controls]","GetLeftIndent method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","GetLeftIndent method","ITextPara.GetLeftIndent","ITextPara::GetLeftIndent","_win32_ITextPara_GetLeftIndent","_win32_ITextPara_GetLeftIndent_cpp","controls.ITextPara_GetLeftIndent","controls._win32_ITextPara_GetLeftIndent","tom/ITextPara::GetLeftIndent"]
old-location: controls\ITextPara_GetLeftIndent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getleftindent.htm
ms.date: 12/05/2018
ms.keywords: GetLeftIndent, GetLeftIndent method [Windows Controls], GetLeftIndent method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetLeftIndent method, ITextPara.GetLeftIndent, ITextPara::GetLeftIndent, _win32_ITextPara_GetLeftIndent, _win32_ITextPara_GetLeftIndent_cpp, controls.ITextPara_GetLeftIndent, controls._win32_ITextPara_GetLeftIndent, tom/ITextPara::GetLeftIndent
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
 - ITextPara::GetLeftIndent
 - tom/ITextPara::GetLeftIndent
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
 - ITextPara.GetLeftIndent
---

# ITextPara::GetLeftIndent


## -description

Retrieves the distance used to indent all lines except the first line of a paragraph. The distance is relative to the left margin.

## -parameters

### -param pValue

Type: <b>float*</b>

The left indentation, in floating-point points.

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::GetLeftIndent</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

To set the left indentation amount, call the <a href="/windows/desktop/api/tom/nf-tom-itextpara-setindents">ITextPara::SetIndents</a> method.

To get the first-line indent, call <a href="/windows/desktop/api/tom/nf-tom-itextpara-getfirstlineindent">ITextPara::GetFirstLineIndent</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getfirstlineindent">GetFirstLineIndent</a>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setindents">SetIndents</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
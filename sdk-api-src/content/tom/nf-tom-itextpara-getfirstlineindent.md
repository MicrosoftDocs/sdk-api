---
UID: NF:tom.ITextPara.GetFirstLineIndent
title: ITextPara::GetFirstLineIndent (tom.h)
description: Retrieves the amount used to indent the first line of a paragraph relative to the left indent. The left indent is the indent for all lines of the paragraph except the first line.
helpviewer_keywords: ["GetFirstLineIndent","GetFirstLineIndent method [Windows Controls]","GetFirstLineIndent method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","GetFirstLineIndent method","ITextPara.GetFirstLineIndent","ITextPara::GetFirstLineIndent","_win32_ITextPara_GetFirstLineIndent","_win32_ITextPara_GetFirstLineIndent_cpp","controls.ITextPara_GetFirstLineIndent","controls._win32_ITextPara_GetFirstLineIndent","tom/ITextPara::GetFirstLineIndent"]
old-location: controls\ITextPara_GetFirstLineIndent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getfirstlineindent.htm
ms.date: 12/05/2018
ms.keywords: GetFirstLineIndent, GetFirstLineIndent method [Windows Controls], GetFirstLineIndent method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetFirstLineIndent method, ITextPara.GetFirstLineIndent, ITextPara::GetFirstLineIndent, _win32_ITextPara_GetFirstLineIndent, _win32_ITextPara_GetFirstLineIndent_cpp, controls.ITextPara_GetFirstLineIndent, controls._win32_ITextPara_GetFirstLineIndent, tom/ITextPara::GetFirstLineIndent
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
 - ITextPara::GetFirstLineIndent
 - tom/ITextPara::GetFirstLineIndent
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
 - ITextPara.GetFirstLineIndent
---

# ITextPara::GetFirstLineIndent


## -description

Retrieves the amount used to indent the first line of a paragraph relative to the left indent. The left indent is the indent for all lines of the paragraph except the first line.

## -parameters

### -param pValue

Type: <b>float*</b>

The first-line indentation amount in floating-point points.

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::GetFirstLineIndent</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes.  For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

To set the first line indentation amount, call the <a href="/windows/desktop/api/tom/nf-tom-itextpara-setindents">ITextPara::SetIndents</a> method.

To get and set the indent for all other lines of the paragraph (that is, the left
				indent), use <a href="/windows/desktop/api/tom/nf-tom-itextpara-getleftindent">ITextPara::GetLeftIndent</a> and <a href="/windows/desktop/api/tom/nf-tom-itextpara-setindents">ITextPara::SetIndents</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getleftindent">GetLeftIndent</a>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setindents">SetIndents</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
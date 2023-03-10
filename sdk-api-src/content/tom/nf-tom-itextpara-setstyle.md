---
UID: NF:tom.ITextPara.SetStyle
title: ITextPara::SetStyle (tom.h)
description: Sets the paragraph style for the paragraphs in a range.
helpviewer_keywords: ["ITextPara interface [Windows Controls]","SetStyle method","ITextPara.SetStyle","ITextPara::SetStyle","SetStyle","SetStyle method [Windows Controls]","SetStyle method [Windows Controls]","ITextPara interface","_win32_ITextPara_SetStyle","_win32_ITextPara_SetStyle_cpp","controls.ITextPara_SetStyle","controls._win32_ITextPara_SetStyle","tom/ITextPara::SetStyle"]
old-location: controls\ITextPara_SetStyle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextpara\itextparasetstyle.htm
ms.date: 12/05/2018
ms.keywords: ITextPara interface [Windows Controls],SetStyle method, ITextPara.SetStyle, ITextPara::SetStyle, SetStyle, SetStyle method [Windows Controls], SetStyle method [Windows Controls],ITextPara interface, _win32_ITextPara_SetStyle, _win32_ITextPara_SetStyle_cpp, controls.ITextPara_SetStyle, controls._win32_ITextPara_SetStyle, tom/ITextPara::SetStyle
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
 - ITextPara::SetStyle
 - tom/ITextPara::SetStyle
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
 - ITextPara.SetStyle
---

# ITextPara::SetStyle


## -description

Sets the paragraph style for the paragraphs in a range.

## -parameters

### -param Value [in]

Type: <b>long</b>

New paragraph style handle. For a list of styles, see the Remarks section of <a href="/windows/desktop/api/tom/nf-tom-itextpara-getstyle">ITextPara::GetStyle</a>.

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::SetStyle</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getstyle">GetStyle</a>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
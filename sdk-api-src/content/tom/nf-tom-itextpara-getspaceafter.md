---
UID: NF:tom.ITextPara.GetSpaceAfter
title: ITextPara::GetSpaceAfter (tom.h)
description: Retrieves the amount of vertical space below a paragraph.
helpviewer_keywords: ["GetSpaceAfter","GetSpaceAfter method [Windows Controls]","GetSpaceAfter method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","GetSpaceAfter method","ITextPara.GetSpaceAfter","ITextPara::GetSpaceAfter","_win32_ITextPara_GetSpaceAfter","_win32_ITextPara_GetSpaceAfter_cpp","controls.ITextPara_GetSpaceAfter","controls._win32_ITextPara_GetSpaceAfter","tom/ITextPara::GetSpaceAfter"]
old-location: controls\ITextPara_GetSpaceAfter.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getspaceafter.htm
ms.date: 12/05/2018
ms.keywords: GetSpaceAfter, GetSpaceAfter method [Windows Controls], GetSpaceAfter method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetSpaceAfter method, ITextPara.GetSpaceAfter, ITextPara::GetSpaceAfter, _win32_ITextPara_GetSpaceAfter, _win32_ITextPara_GetSpaceAfter_cpp, controls.ITextPara_GetSpaceAfter, controls._win32_ITextPara_GetSpaceAfter, tom/ITextPara::GetSpaceAfter
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
 - ITextPara::GetSpaceAfter
 - tom/ITextPara::GetSpaceAfter
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
 - ITextPara.GetSpaceAfter
---

# ITextPara::GetSpaceAfter


## -description

Retrieves the amount of vertical space below a paragraph.

## -parameters

### -param pValue

Type: <b>float*</b>

The space-after value, in floating-point points.

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::GetSpaceAfter</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getspacebefore">GetSpaceBefore</a>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setspaceafter">SetSpaceAfter</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setspacebefore">SetSpaceBefore</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
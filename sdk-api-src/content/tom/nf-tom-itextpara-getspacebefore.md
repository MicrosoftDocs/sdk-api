---
UID: NF:tom.ITextPara.GetSpaceBefore
title: ITextPara::GetSpaceBefore (tom.h)
description: Retrieves the amount of vertical space above a paragraph.
helpviewer_keywords: ["GetSpaceBefore","GetSpaceBefore method [Windows Controls]","GetSpaceBefore method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","GetSpaceBefore method","ITextPara.GetSpaceBefore","ITextPara::GetSpaceBefore","_win32_ITextPara_GetSpaceBefore","_win32_ITextPara_GetSpaceBefore_cpp","controls.ITextPara_GetSpaceBefore","controls._win32_ITextPara_GetSpaceBefore","tom/ITextPara::GetSpaceBefore"]
old-location: controls\ITextPara_GetSpaceBefore.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getspacebefore.htm
ms.date: 12/05/2018
ms.keywords: GetSpaceBefore, GetSpaceBefore method [Windows Controls], GetSpaceBefore method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetSpaceBefore method, ITextPara.GetSpaceBefore, ITextPara::GetSpaceBefore, _win32_ITextPara_GetSpaceBefore, _win32_ITextPara_GetSpaceBefore_cpp, controls.ITextPara_GetSpaceBefore, controls._win32_ITextPara_GetSpaceBefore, tom/ITextPara::GetSpaceBefore
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
 - ITextPara::GetSpaceBefore
 - tom/ITextPara::GetSpaceBefore
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
 - ITextPara.GetSpaceBefore
---

# ITextPara::GetSpaceBefore


## -description

Retrieves the amount of vertical space above a paragraph.

## -parameters

### -param pValue

Type: <b>float*</b>

The space-before value, in floating-point points.

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::GetSpaceBefore</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getspaceafter">GetSpaceAfter</a>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setspaceafter">SetSpaceAfter</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setspacebefore">SetSpaceBefore</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
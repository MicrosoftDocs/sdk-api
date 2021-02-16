---
UID: NF:tom.ITextPara.GetDuplicate
title: ITextPara::GetDuplicate (tom.h)
description: Creates a duplicate of the specified paragraph format object. The duplicate property is the default property of an ITextPara object.
helpviewer_keywords: ["GetDuplicate","GetDuplicate method [Windows Controls]","GetDuplicate method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","GetDuplicate method","ITextPara.GetDuplicate","ITextPara::GetDuplicate","_win32_ITextPara_GetDuplicate","_win32_ITextPara_GetDuplicate_cpp","controls.ITextPara_GetDuplicate","controls._win32_ITextPara_GetDuplicate","tom/ITextPara::GetDuplicate"]
old-location: controls\ITextPara_GetDuplicate.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextpara\itextparagetduplicate.htm
ms.date: 12/05/2018
ms.keywords: GetDuplicate, GetDuplicate method [Windows Controls], GetDuplicate method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetDuplicate method, ITextPara.GetDuplicate, ITextPara::GetDuplicate, _win32_ITextPara_GetDuplicate, _win32_ITextPara_GetDuplicate_cpp, controls.ITextPara_GetDuplicate, controls._win32_ITextPara_GetDuplicate, tom/ITextPara::GetDuplicate
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
 - ITextPara::GetDuplicate
 - tom/ITextPara::GetDuplicate
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
 - ITextPara.GetDuplicate
---

# ITextPara::GetDuplicate


## -description

Creates a duplicate of the specified paragraph format object. The duplicate property is the default property of an <a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a> object.

## -parameters

### -param ppPara

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>**</b>

The duplicate <a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a> object.

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::GetDuplicate</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes.  For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory could not be allocated for the new object.

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



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setduplicate">SetDuplicate</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
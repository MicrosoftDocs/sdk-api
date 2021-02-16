---
UID: NF:tom.ITextPara.SetListLevelIndex
title: ITextPara::SetListLevelIndex (tom.h)
description: Sets the list level index used for paragraphs.
helpviewer_keywords: ["ITextPara interface [Windows Controls]","SetListLevelIndex method","ITextPara.SetListLevelIndex","ITextPara::SetListLevelIndex","SetListLevelIndex","SetListLevelIndex method [Windows Controls]","SetListLevelIndex method [Windows Controls]","ITextPara interface","_win32_ITextPara_SetListLevelIndex","_win32_ITextPara_SetListLevelIndex_cpp","controls.ITextPara_SetListLevelIndex","controls._win32_ITextPara_SetListLevelIndex","tom/ITextPara::SetListLevelIndex"]
old-location: controls\ITextPara_SetListLevelIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setlistlevelindex.htm
ms.date: 12/05/2018
ms.keywords: ITextPara interface [Windows Controls],SetListLevelIndex method, ITextPara.SetListLevelIndex, ITextPara::SetListLevelIndex, SetListLevelIndex, SetListLevelIndex method [Windows Controls], SetListLevelIndex method [Windows Controls],ITextPara interface, _win32_ITextPara_SetListLevelIndex, _win32_ITextPara_SetListLevelIndex_cpp, controls.ITextPara_SetListLevelIndex, controls._win32_ITextPara_SetListLevelIndex, tom/ITextPara::SetListLevelIndex
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
 - ITextPara::SetListLevelIndex
 - tom/ITextPara::SetListLevelIndex
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
 - ITextPara.SetListLevelIndex
---

# ITextPara::SetListLevelIndex


## -description

Sets the list level index used for paragraphs.

## -parameters

### -param Value [in]

Type: <b>long</b>

New list level index value. For possible values, see <a href="/windows/desktop/api/tom/nf-tom-itextpara-getlistlevelindex">ITextPara::GetListLevelIndex</a>.

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::SetListLevelIndex</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

Setting the list level index does not automatically change a list's indentation and other paragraph properties.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getlistlevelindex">GetListLevelIndex</a>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
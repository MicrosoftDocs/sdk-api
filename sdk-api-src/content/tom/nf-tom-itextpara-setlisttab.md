---
UID: NF:tom.ITextPara.SetListTab
title: ITextPara::SetListTab (tom.h)
description: Sets the list tab setting, which is the distance between the first indent and the start of the text on the first line.
helpviewer_keywords: ["ITextPara interface [Windows Controls]","SetListTab method","ITextPara.SetListTab","ITextPara::SetListTab","SetListTab","SetListTab method [Windows Controls]","SetListTab method [Windows Controls]","ITextPara interface","_win32_ITextPara_SetListTab","_win32_ITextPara_SetListTab_cpp","controls.ITextPara_SetListTab","controls._win32_ITextPara_SetListTab","tom/ITextPara::SetListTab"]
old-location: controls\ITextPara_SetListTab.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setlisttab.htm
ms.date: 12/05/2018
ms.keywords: ITextPara interface [Windows Controls],SetListTab method, ITextPara.SetListTab, ITextPara::SetListTab, SetListTab, SetListTab method [Windows Controls], SetListTab method [Windows Controls],ITextPara interface, _win32_ITextPara_SetListTab, _win32_ITextPara_SetListTab_cpp, controls.ITextPara_SetListTab, controls._win32_ITextPara_SetListTab, tom/ITextPara::SetListTab
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
 - ITextPara::SetListTab
 - tom/ITextPara::SetListTab
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
 - ITextPara.SetListTab
---

# ITextPara::SetListTab


## -description

Sets the list tab setting, which is the distance between the first indent and the start of the text on the first line.

## -parameters

### -param Value [in]

Type: <b>float</b>

New list tab value, in floating-point points.

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::SetListTab</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

<a href="/windows/desktop/api/tom/nf-tom-itextpara-addtab">AddTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-clearalltabs">ClearAllTabs</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-deletetab">DeleteTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getlisttab">GetListTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-gettab">GetTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-gettabcount">GetTabCount</a>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
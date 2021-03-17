---
UID: NF:tom.ITextPara.GetListTab
title: ITextPara::GetListTab (tom.h)
description: Retrieves the list tab setting, which is the distance between the first-line indent and the text on the first line. The numbered or bulleted text is left-justified, centered, or right-justified at the first-line indent value.
helpviewer_keywords: ["GetListTab","GetListTab method [Windows Controls]","GetListTab method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","GetListTab method","ITextPara.GetListTab","ITextPara::GetListTab","_win32_ITextPara_GetListTab","_win32_ITextPara_GetListTab_cpp","controls.ITextPara_GetListTab","controls._win32_ITextPara_GetListTab","tom/ITextPara::GetListTab"]
old-location: controls\ITextPara_GetListTab.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getlisttab.htm
ms.date: 12/05/2018
ms.keywords: GetListTab, GetListTab method [Windows Controls], GetListTab method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetListTab method, ITextPara.GetListTab, ITextPara::GetListTab, _win32_ITextPara_GetListTab, _win32_ITextPara_GetListTab_cpp, controls.ITextPara_GetListTab, controls._win32_ITextPara_GetListTab, tom/ITextPara::GetListTab
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
 - ITextPara::GetListTab
 - tom/ITextPara::GetListTab
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
 - ITextPara.GetListTab
---

# ITextPara::GetListTab


## -description

Retrieves the list tab setting, which is the distance between the first-line indent and the text on the first line. The numbered or bulleted text is left-justified, centered, or right-justified at the first-line indent value.

## -parameters

### -param pValue

Type: <b>float*</b>

The list tab setting. The list tab value is in floating-point points.

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::GetListTab</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

To determine whether the numbered or bulleted text is left-justified, centered, or right-justified, call <a href="/windows/desktop/api/tom/nf-tom-itextpara-getlistalignment">ITextPara::GetListAlignment</a>.

## -see-also

<a href="/windows/desktop/api/tom/nf-tom-itextpara-addtab">AddTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-clearalltabs">ClearAllTabs</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-deletetab">DeleteTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getfirstlineindent">GetFirstLineIndent</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getlistalignment">GetListAlignment</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-gettab">GetTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-gettabcount">GetTabCount</a>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setlisttab">SetListTab</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
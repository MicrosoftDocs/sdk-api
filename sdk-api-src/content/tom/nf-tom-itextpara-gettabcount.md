---
UID: NF:tom.ITextPara.GetTabCount
title: ITextPara::GetTabCount (tom.h)
description: Retrieves the tab count.
helpviewer_keywords: ["GetTabCount","GetTabCount method [Windows Controls]","GetTabCount method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","GetTabCount method","ITextPara.GetTabCount","ITextPara::GetTabCount","_win32_ITextPara_GetTabCount","_win32_ITextPara_GetTabCount_cpp","controls.ITextPara_GetTabCount","controls._win32_ITextPara_GetTabCount","tom/ITextPara::GetTabCount"]
old-location: controls\ITextPara_GetTabCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\gettabcount.htm
ms.date: 12/05/2018
ms.keywords: GetTabCount, GetTabCount method [Windows Controls], GetTabCount method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetTabCount method, ITextPara.GetTabCount, ITextPara::GetTabCount, _win32_ITextPara_GetTabCount, _win32_ITextPara_GetTabCount_cpp, controls.ITextPara_GetTabCount, controls._win32_ITextPara_GetTabCount, tom/ITextPara::GetTabCount
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
 - ITextPara::GetTabCount
 - tom/ITextPara::GetTabCount
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
 - ITextPara.GetTabCount
---

# ITextPara::GetTabCount


## -description

Retrieves the tab count.

## -parameters

### -param pCount

Type: <b>long*</b>

The tab count.

## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::GetTabCount</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

The tab count of a new instance can be nonzero, depending on the underlying text engine. For example, Microsoft Word stories begin with no explicit tabs defined, while rich edit instances start with a single explicit tab. To be sure there are no explicit tabs (that is, to set the tab count to zero), call <a href="/windows/desktop/api/tom/nf-tom-itextpara-clearalltabs">ITextPara::ClearAllTabs</a>.

## -see-also

<a href="/windows/desktop/api/tom/nf-tom-itextpara-addtab">AddTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-clearalltabs">ClearAllTabs</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-deletetab">DeleteTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getlisttab">GetListTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-gettab">GetTab</a>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setlisttab">SetListTab</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
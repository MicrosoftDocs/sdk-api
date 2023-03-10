---
UID: NF:tom.ITextPara.ClearAllTabs
title: ITextPara::ClearAllTabs (tom.h)
description: Clears all tabs, reverting to equally spaced tabs with the default tab spacing.
helpviewer_keywords: ["ClearAllTabs","ClearAllTabs method [Windows Controls]","ClearAllTabs method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","ClearAllTabs method","ITextPara.ClearAllTabs","ITextPara::ClearAllTabs","_win32_ITextPara_ClearAllTabs","_win32_ITextPara_ClearAllTabs_cpp","controls.ITextPara_ClearAllTabs","controls._win32_ITextPara_ClearAllTabs","tom/ITextPara::ClearAllTabs"]
old-location: controls\ITextPara_ClearAllTabs.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\clearalltabs.htm
ms.date: 12/05/2018
ms.keywords: ClearAllTabs, ClearAllTabs method [Windows Controls], ClearAllTabs method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],ClearAllTabs method, ITextPara.ClearAllTabs, ITextPara::ClearAllTabs, _win32_ITextPara_ClearAllTabs, _win32_ITextPara_ClearAllTabs_cpp, controls.ITextPara_ClearAllTabs, controls._win32_ITextPara_ClearAllTabs, tom/ITextPara::ClearAllTabs
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
 - ITextPara::ClearAllTabs
 - tom/ITextPara::ClearAllTabs
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
 - ITextPara.ClearAllTabs
---

# ITextPara::ClearAllTabs


## -description

Clears all tabs, reverting to equally spaced tabs with the default tab spacing.



## -returns

Type: <b>HRESULT</b>

If <b>ITextPara::ClearAllTabs</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes.  For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
The paragraph format object is attached to a range that has been deleted.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tom/nf-tom-itextpara-addtab">AddTab</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-deletetab">DeleteTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument-getdefaulttabstop">GetDefaultTabStop</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getlisttab">GetListTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-gettab">GetTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-gettabcount">GetTabCount</a>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setlisttab">SetListTab</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>

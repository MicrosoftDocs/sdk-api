---
UID: NF:tom.ITextDocument.SetDefaultTabStop
title: ITextDocument::SetDefaultTabStop (tom.h)
description: Sets the default tab stop, which is used when no tab exists beyond the current display position.
helpviewer_keywords: ["ITextDocument interface [Windows Controls]","SetDefaultTabStop method","ITextDocument.SetDefaultTabStop","ITextDocument::SetDefaultTabStop","SetDefaultTabStop","SetDefaultTabStop method [Windows Controls]","SetDefaultTabStop method [Windows Controls]","ITextDocument interface","_win32_ITextDocument_SetDefaultTabStop","_win32_ITextDocument_SetDefaultTabStop_cpp","controls.ITextDocument_SetDefaultTabStop","controls._win32_ITextDocument_SetDefaultTabStop","tom/ITextDocument::SetDefaultTabStop"]
old-location: controls\ITextDocument_SetDefaultTabStop.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setdefaulttabstop.htm
ms.date: 12/05/2018
ms.keywords: ITextDocument interface [Windows Controls],SetDefaultTabStop method, ITextDocument.SetDefaultTabStop, ITextDocument::SetDefaultTabStop, SetDefaultTabStop, SetDefaultTabStop method [Windows Controls], SetDefaultTabStop method [Windows Controls],ITextDocument interface, _win32_ITextDocument_SetDefaultTabStop, _win32_ITextDocument_SetDefaultTabStop_cpp, controls.ITextDocument_SetDefaultTabStop, controls._win32_ITextDocument_SetDefaultTabStop, tom/ITextDocument::SetDefaultTabStop
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
 - ITextDocument::SetDefaultTabStop
 - tom/ITextDocument::SetDefaultTabStop
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
 - ITextDocument.SetDefaultTabStop
---

# ITextDocument::SetDefaultTabStop


## -description

Sets the default tab stop, which is used when no tab exists beyond the current display position.

## -parameters

### -param Value [in]

Type: <b>float</b>

New default tab setting, in floating-point points. Default value is 36.0 points, that is, 0.5 inches.

## -returns

Type: <b>HRESULT</b>

If the method succeeds it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tom/nf-tom-itextpara-addtab">AddTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-clearalltabs">ClearAllTabs</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-deletetab">DeleteTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument-getdefaulttabstop">GetDefaultTabStop</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getlisttab">GetListTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-gettab">GetTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-gettabcount">GetTabCount</a>



<a href="/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setlisttab">SetListTab</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
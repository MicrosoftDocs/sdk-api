---
UID: NF:tom.ITextDocument.GetDefaultTabStop
title: ITextDocument::GetDefaultTabStop (tom.h)
description: Gets the default tab width.
helpviewer_keywords: ["GetDefaultTabStop","GetDefaultTabStop method [Windows Controls]","GetDefaultTabStop method [Windows Controls]","ITextDocument interface","ITextDocument interface [Windows Controls]","GetDefaultTabStop method","ITextDocument.GetDefaultTabStop","ITextDocument::GetDefaultTabStop","_win32_ITextDocument_GetDefaultTabStop","_win32_ITextDocument_GetDefaultTabStop_cpp","controls.ITextDocument_GetDefaultTabStop","controls._win32_ITextDocument_GetDefaultTabStop","tom/ITextDocument::GetDefaultTabStop"]
old-location: controls\ITextDocument_GetDefaultTabStop.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getdefaulttabstop.htm
ms.date: 12/05/2018
ms.keywords: GetDefaultTabStop, GetDefaultTabStop method [Windows Controls], GetDefaultTabStop method [Windows Controls],ITextDocument interface, ITextDocument interface [Windows Controls],GetDefaultTabStop method, ITextDocument.GetDefaultTabStop, ITextDocument::GetDefaultTabStop, _win32_ITextDocument_GetDefaultTabStop, _win32_ITextDocument_GetDefaultTabStop_cpp, controls.ITextDocument_GetDefaultTabStop, controls._win32_ITextDocument_GetDefaultTabStop, tom/ITextDocument::GetDefaultTabStop
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
 - ITextDocument::GetDefaultTabStop
 - tom/ITextDocument::GetDefaultTabStop
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
 - ITextDocument.GetDefaultTabStop
---

# ITextDocument::GetDefaultTabStop


## -description

Gets the default tab width.

## -parameters

### -param pValue

Type: <b>float*</b>

The default tab width.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If 
						<i>pValue</i> is <b>NULL</b>, the method fails and it returns <b>E_INVALIDARG</b>. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

## -remarks

The default tab width is used whenever no tab exists beyond the current display position. The default width is given in floating-point points.

## -see-also

<a href="/windows/desktop/api/tom/nf-tom-itextpara-addtab">AddTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-clearalltabs">ClearAllTabs</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-deletetab">DeleteTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-getlisttab">GetListTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-gettab">GetTab</a>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-gettabcount">GetTabCount</a>



<a href="/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextpara-setlisttab">SetListTab</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
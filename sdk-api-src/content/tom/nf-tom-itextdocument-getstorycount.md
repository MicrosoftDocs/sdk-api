---
UID: NF:tom.ITextDocument.GetStoryCount
title: ITextDocument::GetStoryCount (tom.h)
description: Gets the count of stories in this document.
helpviewer_keywords: ["GetStoryCount","GetStoryCount method [Windows Controls]","GetStoryCount method [Windows Controls]","ITextDocument interface","ITextDocument interface [Windows Controls]","GetStoryCount method","ITextDocument.GetStoryCount","ITextDocument::GetStoryCount","_win32_ITextDocument_GetStoryCount","_win32_ITextDocument_GetStoryCount_cpp","controls.ITextDocument_GetStoryCount","controls._win32_ITextDocument_GetStoryCount","tom/ITextDocument::GetStoryCount"]
old-location: controls\ITextDocument_GetStoryCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getstorycount.htm
ms.date: 12/05/2018
ms.keywords: GetStoryCount, GetStoryCount method [Windows Controls], GetStoryCount method [Windows Controls],ITextDocument interface, ITextDocument interface [Windows Controls],GetStoryCount method, ITextDocument.GetStoryCount, ITextDocument::GetStoryCount, _win32_ITextDocument_GetStoryCount, _win32_ITextDocument_GetStoryCount_cpp, controls.ITextDocument_GetStoryCount, controls._win32_ITextDocument_GetStoryCount, tom/ITextDocument::GetStoryCount
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
 - ITextDocument::GetStoryCount
 - tom/ITextDocument::GetStoryCount
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
 - ITextDocument.GetStoryCount
---

# ITextDocument::GetStoryCount


## -description

Gets the count of stories in this document.

## -parameters

### -param pCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a>*</b>

The number of stories in the document.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns the following COM error code. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
</table>

## -remarks

Rich edit controls have only one story and do not implement the <a href="/windows/desktop/api/tom/nf-tom-itextdocument-getstoryranges">ITextDocument::GetStoryRanges</a> method. To avoid getting an error when there is only one story, use <b>ITextDocument::GetStoryCount</b> to check the story count. If the story count is greater than one, then call 
				<b>ITextDocument::GetStoryRanges</b>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextdocument-getstoryranges">GetStoryRanges</a>



<a href="/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
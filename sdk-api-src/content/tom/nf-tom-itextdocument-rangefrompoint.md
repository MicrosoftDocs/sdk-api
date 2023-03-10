---
UID: NF:tom.ITextDocument.RangeFromPoint
title: ITextDocument::RangeFromPoint (tom.h)
description: Retrieves a range for the content at or nearest to the specified point on the screen.
helpviewer_keywords: ["ITextDocument interface [Windows Controls]","RangeFromPoint method","ITextDocument.RangeFromPoint","ITextDocument::RangeFromPoint","RangeFromPoint","RangeFromPoint method [Windows Controls]","RangeFromPoint method [Windows Controls]","ITextDocument interface","_win32_ITextDocument_RangeFromPoint","_win32_ITextDocument_RangeFromPoint_cpp","controls.ITextDocument_RangeFromPoint","controls._win32_ITextDocument_RangeFromPoint","tom/ITextDocument::RangeFromPoint"]
old-location: controls\ITextDocument_RangeFromPoint.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\rangefrompoint.htm
ms.date: 12/05/2018
ms.keywords: ITextDocument interface [Windows Controls],RangeFromPoint method, ITextDocument.RangeFromPoint, ITextDocument::RangeFromPoint, RangeFromPoint, RangeFromPoint method [Windows Controls], RangeFromPoint method [Windows Controls],ITextDocument interface, _win32_ITextDocument_RangeFromPoint, _win32_ITextDocument_RangeFromPoint_cpp, controls.ITextDocument_RangeFromPoint, controls._win32_ITextDocument_RangeFromPoint, tom/ITextDocument::RangeFromPoint
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
 - ITextDocument::RangeFromPoint
 - tom/ITextDocument::RangeFromPoint
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
 - ITextDocument.RangeFromPoint
---

# ITextDocument::RangeFromPoint


## -description

Retrieves a range for the content at or nearest to the specified point on the screen.

## -parameters

### -param x

Type: <b>long</b>

The horizontal coordinate of the specified point, in screen coordinates.

### -param y

Type: <b>long</b>

The vertical coordinate of the specified point, in screen coordinates.

### -param ppRange

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>**</b>

The text range that corresponds to the specified point.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-expand">Expand</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-getpoint">GetPoint</a>



<a href="/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-movestart">MoveStart</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
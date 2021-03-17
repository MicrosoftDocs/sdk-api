---
UID: NF:tom.ITextRange.GetDuplicate
title: ITextRange::GetDuplicate (tom.h)
description: Gets a duplicate of this range object.
helpviewer_keywords: ["GetDuplicate","GetDuplicate method [Windows Controls]","GetDuplicate method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","GetDuplicate method","ITextRange.GetDuplicate","ITextRange::GetDuplicate","_win32_ITextRange_GetDuplicate","_win32_ITextRange_GetDuplicate_cpp","controls.ITextRange_GetDuplicate","controls._win32_ITextRange_GetDuplicate","tom/ITextRange::GetDuplicate"]
old-location: controls\ITextRange_GetDuplicate.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextrange\itextrangegetduplicate.htm
ms.date: 12/05/2018
ms.keywords: GetDuplicate, GetDuplicate method [Windows Controls], GetDuplicate method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetDuplicate method, ITextRange.GetDuplicate, ITextRange::GetDuplicate, _win32_ITextRange_GetDuplicate, _win32_ITextRange_GetDuplicate_cpp, controls.ITextRange_GetDuplicate, controls._win32_ITextRange_GetDuplicate, tom/ITextRange::GetDuplicate
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
 - ITextRange::GetDuplicate
 - tom/ITextRange::GetDuplicate
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
 - ITextRange.GetDuplicate
---

# ITextRange::GetDuplicate


## -description

Gets a duplicate of this range object.

## -parameters

### -param ppRange

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>**</b>

The duplicate of the range.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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
ppRange is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure for some other reason.

</td>
</tr>
</table>

## -remarks

To create an insertion point in order to traverse a range, first duplicate the range and then collapse the duplicate at its start character position. Note, a range is characterized by start and end character positions, and the story it belongs to.

Even if the range is actually an <a href="/windows/desktop/api/tom/nn-tom-itextselection">ITextSelection</a>, the duplicate returned is an <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>. For an example, see the <a href="/windows/desktop/api/tom/nf-tom-itextrange-findtext">ITextRange::FindText</a> method.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-findtext">FindText</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
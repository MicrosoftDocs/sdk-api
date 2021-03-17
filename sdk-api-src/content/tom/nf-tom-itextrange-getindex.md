---
UID: NF:tom.ITextRange.GetIndex
title: ITextRange::GetIndex (tom.h)
description: Retrieves the story index of the Unit parameter at the specified range Start character position.
helpviewer_keywords: ["GetIndex","GetIndex method [Windows Controls]","GetIndex method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","GetIndex method","ITextRange.GetIndex","ITextRange::GetIndex","_win32_ITextRange_GetIndex","_win32_ITextRange_GetIndex_cpp","controls.ITextRange_GetIndex","controls._win32_ITextRange_GetIndex","tom/ITextRange::GetIndex"]
old-location: controls\ITextRange_GetIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getindex.htm
ms.date: 12/05/2018
ms.keywords: GetIndex, GetIndex method [Windows Controls], GetIndex method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetIndex method, ITextRange.GetIndex, ITextRange::GetIndex, _win32_ITextRange_GetIndex, _win32_ITextRange_GetIndex_cpp, controls.ITextRange_GetIndex, controls._win32_ITextRange_GetIndex, tom/ITextRange::GetIndex
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
 - ITextRange::GetIndex
 - tom/ITextRange::GetIndex
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
 - ITextRange.GetIndex
---

# ITextRange::GetIndex


## -description

Retrieves the story index of the <i>Unit</i> parameter at the specified range Start character position. The first <i>Unit</i> in a story has an index value of 1. The index of a <i>Unit</i> is the same for all character positions from that immediately preceding the <i>Unit</i> up to the last character in the <i>Unit</i>.

## -parameters

### -param Unit

Type: <b>long</b>

Unit that is indexed. For a list of possible <i>Unit</i> values, see the discussion under <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>.

### -param pIndex

Type: <b>long*</b>

The index value. The value is zero if <i>Unit</i> does not exist.

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
<i>pIndex</i> is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Unit does not exist.

</td>
</tr>
</table>

## -remarks

The <b>ITextRange::GetIndex</b> method retrieves the story index of a word, line, sentence, paragraph, and so forth, at the range Start. <i>Unit</i> specifies which kind of entity to index, such as words (<b>tomWord</b>), lines (<b>tomLine</b>), sentences (<b>tomSentence</b>), or paragraphs (<b>tomParagraph</b>). For example, <b>ITextRange::GetIndex</b> sets <i>pIndex</i> equal to the line number of the first line in the range. For a range at the end of the story, <b>ITextRange::GetIndex</b>, returns the number of <i>Unit</i>s in the story. Thus, you can get the number of words, lines, objects, and so forth, in a story.

The index value returned by the <b>ITextRange::GetIndex</b> method is not valid if the text is subsequently edited. Thus, users should be careful about using methods that return index values, especially if the values are to be stored for any duration. This is in contrast to a pointer to a range, which does remain valid when the text is edited.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
---
UID: NF:tom.ITextRange.InRange
title: ITextRange::InRange (tom.h)
description: Determines whether this range is within or at the same text as a specified range.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","InRange method","ITextRange.InRange","ITextRange::InRange","InRange","InRange method [Windows Controls]","InRange method [Windows Controls]","ITextRange interface","_win32_ITextRange_InRange","_win32_ITextRange_InRange_cpp","controls.ITextRange_InRange","controls._win32_ITextRange_InRange","tom/ITextRange::InRange"]
old-location: controls\ITextRange_InRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\inrange.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],InRange method, ITextRange.InRange, ITextRange::InRange, InRange, InRange method [Windows Controls], InRange method [Windows Controls],ITextRange interface, _win32_ITextRange_InRange, _win32_ITextRange_InRange_cpp, controls.ITextRange_InRange, controls._win32_ITextRange_InRange, tom/ITextRange::InRange
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
 - ITextRange::InRange
 - tom/ITextRange::InRange
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
 - ITextRange.InRange
---

# ITextRange::InRange


## -description

Determines whether this range is within or at the same text as a specified range.

## -parameters

### -param pRange

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>*</b>

Text that is compared to the current range.

### -param pValue

Type: <b>long*</b>

The comparison result. The pointer can be null. The method returns <i>pB</i> is <b>tomTrue</b> only if the range is in or at the same text as <i>pRange</i>.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns S_FALSE.

## -remarks

For range2 to be contained in range1, both ranges must be in the same story, and the limits of 
				range2 must satisfy 
				either of the following statements. 

<ul>
<li>The start and end character positions of range1 are the same as range2. That is, both ranges are degenerate and have identical insertion points. </li>
<li>Range2 is a nondegenerate range with start and end character positions at or within those of range1. </li>
</ul>
The following example shows how to walk one range with another. 


```
    range2 = range1.Duplicate
    range2.End = range2.Start       ' Collapse range2 to its start position 
    While range2.InRange(range1)    ' Iterate so long as range2 remains within range1
         ...   ' This code would change the range2 character positions 
    Wend
```


When the <a href="/windows/desktop/api/tom/nf-tom-itextrange-findtext">ITextRange::FindText</a>, <a href="/windows/desktop/api/tom/nf-tom-itextrange-movewhile">ITextRange::MoveWhile</a>, and <a href="/windows/desktop/api/tom/nf-tom-itextrange-moveuntil">ITextRange::MoveUntil</a> method families are used, you can use one range to walk another by specifying the appropriate limit count of characters (for an example, see the Remarks in 
				<b>ITextRange::Find</b>).


<a href="/windows/desktop/api/tom/nf-tom-itextrange-isequal">ITextRange::IsEqual</a> is a special case of <b>ITextRange::InRange</b> that returns <i>pB</i> <b>tomTrue</b> if the <i>pRange</i> has the same start and end character positions and belongs to the same story.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-findtext">FindText</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-moveuntil">MoveUntil</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-movewhile">MoveWhile</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
---
UID: NF:tom.ITextRange.InRange
title: ITextRange::InRange
author: windows-sdk-content
description: Determines whether this range is within or at the same text as a specified range.
old-location: controls\ITextRange_InRange.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\inrange.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: ITextRange interface [Windows Controls],InRange method, ITextRange.InRange, ITextRange::InRange, InRange, InRange method [Windows Controls], InRange method [Windows Controls],ITextRange interface, _win32_ITextRange_InRange, _win32_ITextRange_InRange_cpp, controls.ITextRange_InRange, controls._win32_ITextRange_InRange, tom/ITextRange::InRange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextRange.InRange
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange::InRange


## -description


Determines whether this range is within or at the same text as a specified range. 


## -parameters




### -param pRange

Type: <b><a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>*</b>

Text that is compared to the current range. 


### -param pValue






#### - pB

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
<li>
						The start and end character positions of range1 are the same as range2. That is, both ranges are degenerate and have identical insertion points. </li>
<li>Range2 is a nondegenerate range with start and end character positions at or within those of range1. </li>
</ul>
The following example shows how to walk one range with another. 

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>    range2 = range1.Duplicate
    range2.End = range2.Start       ' Collapse range2 to its start position 
    While range2.InRange(range1)    ' Iterate so long as range2 remains within range1
         ...   ' This code would change the range2 character positions 
    Wend</pre>
</td>
</tr>
</table></span></div>
When the <a href="https://msdn.microsoft.com/e0c95f5b-e147-4c1f-ae1a-def36b0be5c1">ITextRange::FindText</a>, <a href="https://msdn.microsoft.com/6cc1c3f9-d5b0-41b3-808e-0df78dc79f67">ITextRange::MoveWhile</a>, and <a href="https://msdn.microsoft.com/a35bdd47-fa5c-4260-8d99-14b0bd4694dd">ITextRange::MoveUntil</a> method families are used, you can use one range to walk another by specifying the appropriate limit count of characters (for an example, see the Remarks in 
				<b>ITextRange::Find</b>).


<a href="https://msdn.microsoft.com/beb9eeec-7edd-4569-91f5-3ec0407240fe">ITextRange::IsEqual</a> is a special case of <b>ITextRange::InRange</b> that returns <i>pB</i> <b>tomTrue</b> if the <i>pRange</i> has the same start and end character positions and belongs to the same story.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e0c95f5b-e147-4c1f-ae1a-def36b0be5c1">FindText</a>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<a href="https://msdn.microsoft.com/a35bdd47-fa5c-4260-8d99-14b0bd4694dd">MoveUntil</a>



<a href="https://msdn.microsoft.com/6cc1c3f9-d5b0-41b3-808e-0df78dc79f67">MoveWhile</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 


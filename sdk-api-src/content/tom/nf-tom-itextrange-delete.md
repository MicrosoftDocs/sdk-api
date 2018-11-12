---
UID: NF:tom.ITextRange.Delete
title: ITextRange::Delete
author: windows-sdk-content
description: Mimics the DELETE and BACKSPACE keys, with and without the CTRL key depressed.
old-location: controls\ITextRange_Delete.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\delete.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: Delete, Delete method [Windows Controls], Delete method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],Delete method, ITextRange.Delete, ITextRange::Delete, _win32_ITextRange_Delete, _win32_ITextRange_Delete_cpp, controls.ITextRange_Delete, controls._win32_ITextRange_Delete, tom/ITextRange::Delete
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange.Delete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange::Delete


## -description


Mimics the DELETE and BACKSPACE keys, with and without the CTRL key depressed. 


## -parameters




### -param Unit

Type: <b>long</b>

Unit to use. 
					<i>Unit</i> can be <i>tomCharacter</i> (the default value) or <i>tomWord</i>. 


### -param Count

Type: <b>long</b>

Number of 
					<i>Unit</i>s to delete. If 
					<i>Count</i>= zero, it deletes the text in the range only. If 
					<i>Count</i> is greater than zero, <b>ITextRange::Delete</b> acts as if the DELETE key was pressed 
					<i>Count</i> times. If 
					<i>Count</i> is less than zero, it acts as if the BACKSPACE key was pressed 
					<i>Count</i> times. The default value is 1. For more information, see the Remarks.


### -param pDelta

Type: <b>long*</b>

The count of units deleted. It can be null. The
					<i>pDelta</i> parameter is set equal to the number of 
					<i>Unit</i>s deleted. Deleting the text in a nondegenerate range counts as one 
					<i>Unit</i>. 


## -returns



Type: <b>HRESULT</b>

This method returns an 
						<b>HRESULT</b> value. If successful, it returns <b>S_OK</b>. Otherwise it returns one of the following values. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Text is write-protected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Failure for some other reason.

</td>
</tr>
</table>
 




## -remarks



If 
				<i>Count</i> = zero, this method deletes the text in the range, that is, it deletes nothing if the range is only an insertion point. 

If 
				<i>Count</i> is not zero, and the range is an insertion point (that is, degenerate), |
				<i>Count</i>| (absolute value of 
				<i>Count</i>)
				<i>Unit</i>s are deleted in the logical direction given by the sign of 
				<i>Count</i>, where a positive value is the direction toward the end of the story, and a negative value is toward the start of the story. 

If 
				<i>Count</i> is not zero, and the range is nondegenerate (contains text), the text in the range is deleted (regardless of the values of 
				<i>Unit </i>and 
				<i>Count</i>), thereby creating an insertion point. Then, |
				<i>Count</i>| - 1
				 
				<i>Unit</i>s are deleted in the logical direction given by the sign of 
				<i>Count</i>. 

The text in the range can also be deleted by assigning a null string to the range (executing statement r = where r is the range). However, <b>ITextRange::Delete</b> does not require allocating a <b>BSTR</b>.

Deleting the end-of-paragraph mark (CR) results in the special behavior of the Microsoft Word UI. Four cases are of particular interest: 

<ul>
<li>If you delete just the CR but the paragraph includes text, then the CR is deleted, and the following paragraph gets the same paragraph formatting as current one. </li>
<li>If you delete the CR as well as some, but not all, of the characters in the following paragraph, the characters left over from the current paragraph get the paragraph formatting of the following paragraph. </li>
<li>If you select to the end of a paragraph, but not the whole paragraph, the CR is not deleted. </li>
<li>If you delete the whole paragraph (from the beginning through the CR), you delete the CR as well (unless it is the final CR in the file). </li>
</ul>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 


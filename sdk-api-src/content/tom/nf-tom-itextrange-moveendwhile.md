---
UID: NF:tom.ITextRange.MoveEndWhile
title: ITextRange::MoveEndWhile
author: windows-sdk-content
description: Moves the end of the range either Count characters or just past all contiguous characters that are found in the set of characters specified by Cset, whichever is less.
old-location: controls\ITextRange_MoveEndWhile.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\moveendwhile.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ITextRange interface [Windows Controls],MoveEndWhile method, ITextRange.MoveEndWhile, ITextRange::MoveEndWhile, MoveEndWhile, MoveEndWhile method [Windows Controls], MoveEndWhile method [Windows Controls],ITextRange interface, _win32_ITextRange_MoveEndWhile, _win32_ITextRange_MoveEndWhile_cpp, controls.ITextRange_MoveEndWhile, controls._win32_ITextRange_MoveEndWhile, tom/ITextRange::MoveEndWhile
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
tech.root: 
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange.MoveEndWhile
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange::MoveEndWhile


## -description


Moves the end of the range either <i>Count</i> characters or just past all contiguous characters that are found in the set of characters specified by <i>Cset</i>, whichever is less. 


## -parameters




### -param Cset

Type: <b>VARIANT*</b>

The character set to use in the match. This could be an explicit string of characters or a character-set index. For more information, see <a href="About_Text_Object_Model.htm">Character Match Sets</a>. 


### -param Count

Type: <b>long</b>

Maximum number of characters to move past. The default value is <b>tomForward</b>, which searches to the end of the story. If <i>Count</i> is greater than zero, the search moves forward (toward the end of the story). If <i>Count</i> is less than zero, the search moves backward (toward the beginning of the story). If  <i>Count</i> is zero, the end position is unchanged.


### -param pDelta

Type: <b>long*</b>

The actual number of characters that the end is moved. The value can be null. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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
Cset is not valid.

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



If the new end precedes the old start, the new start is set equal to the new end.

The motion described by <b>ITextRange::MoveEndWhile</b> is logical rather than geometric. That is, motion is toward the end or toward the start of a story. Depending on the language, moving to the end of the story could be moving left or moving right. 

For more information, see <a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a> and <a href="https://msdn.microsoft.com/e1f22fc3-f8b8-465e-9684-94ddd2875be2">ITextRange::Move</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<a href="https://msdn.microsoft.com/e1f22fc3-f8b8-465e-9684-94ddd2875be2">Move</a>



<a href="https://msdn.microsoft.com/6cc1c3f9-d5b0-41b3-808e-0df78dc79f67">MoveWhile</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 


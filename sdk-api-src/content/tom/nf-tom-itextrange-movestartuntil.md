---
UID: NF:tom.ITextRange.MoveStartUntil
title: ITextRange::MoveStartUntil
author: windows-sdk-content
description: Moves the start position of the range the position of the first character found that is in the set of characters specified by Cset, provided that the character is found within Count characters of the start position.
old-location: controls\ITextRange_MoveStartUntil.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\movestartuntil.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ITextRange interface [Windows Controls],MoveStartUntil method, ITextRange.MoveStartUntil, ITextRange::MoveStartUntil, MoveStartUntil, MoveStartUntil method [Windows Controls], MoveStartUntil method [Windows Controls],ITextRange interface, _win32_ITextRange_MoveStartUntil, _win32_ITextRange_MoveStartUntil_cpp, controls.ITextRange_MoveStartUntil, controls._win32_ITextRange_MoveStartUntil, tom/ITextRange::MoveStartUntil
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
 - ITextRange.MoveStartUntil
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange::MoveStartUntil


## -description


Moves the start position of the range the position of the first character found that is in the set of characters specified by <i>Cset</i>, provided that the character is found within <i>Count</i> characters of the start position.


## -parameters




### -param Cset

Type: <b>VARIANT*</b>

The character set to use in the match. This could be an explicit string of characters or a character-set index. For more information, see <a href="About_Text_Object_Model.htm">Character Match Sets</a>. 


### -param Count

Type: <b>long</b>

Maximum number of characters to move past. The default value is <b>tomForward</b>, which searches to the end of the story. If <i>Count</i> is greater than zero, the search is forward—toward the end of the story—and if <i>Count</i> is less than zero, search is backward—toward the beginning. If  <i>Count</i> is zero, the start position is unchanged.


### -param pDelta

Type: <b>long*</b>

The actual number of characters the start of the range is moved, plus 1 for a match if <i>Count</i> is greater than zero, and –1 for a match if <i>Count</i> is less than zero. The value can be null. 


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



If no character from 
				<i>Cset</i> is found within 
				<i>Count</i> positions of the start position, the range is left unchanged. 

If the new start follows the old end, the new end is set equal to the new start.

The motion described by <b>ITextRange::MoveStartUntil</b> is logical rather than geometric. That is, motion is toward the end or toward the start of a story. Depending on the language, moving to the end of the story could be moving left or moving right. 

For more information, see <a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a> and <a href="https://msdn.microsoft.com/e1f22fc3-f8b8-465e-9684-94ddd2875be2">ITextRange::Move</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<a href="https://msdn.microsoft.com/e1f22fc3-f8b8-465e-9684-94ddd2875be2">Move</a>



<a href="https://msdn.microsoft.com/a35bdd47-fa5c-4260-8d99-14b0bd4694dd">MoveUntil</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 


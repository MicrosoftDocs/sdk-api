---
UID: NF:tom.ITextRange.MoveStart
title: ITextRange::MoveStart
author: windows-sdk-content
description: Moves the start postion of the range the specified number of units in the specified direction.
old-location: controls\ITextRange_MoveStart.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\movestart.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITextRange interface [Windows Controls],MoveStart method, ITextRange.MoveStart, ITextRange::MoveStart, MoveStart, MoveStart method [Windows Controls], MoveStart method [Windows Controls],ITextRange interface, _win32_ITextRange_MoveStart, _win32_ITextRange_MoveStart_cpp, controls.ITextRange_MoveStart, controls._win32_ITextRange_MoveStart, tom/ITextRange::MoveStart
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
 - ITextRange.MoveStart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange::MoveStart


## -description


Moves the start postion of the range the specified number of units in the specified direction. 


## -parameters




### -param Unit

Type: <b>long</b>

Unit used in the move. The default value is <b>tomCharacter</b>. For a list of the other <i>Unit</i> values, see the discussion under <a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>. 


### -param Count

Type: <b>long</b>

Number of units to move. The default value is 1. If <i>Count</i> is greater than zero, motion is forward—toward the end of the story—and if <i>Count</i> is less than zero, motion is backward—toward the beginning. If  <i>Count</i> is zero, the start position is unchanged.


### -param pDelta

Type: <b>long*</b>

The actual number of units that the end is moved. The value can be null. 


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Unit is not supported.

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



If the new start follows the old end, the new end is set equal to the new start.

The motion described by <b>ITextRange::MoveStart</b> is logical rather than geometric. That is, motion is toward the end or toward the start of a story. Depending on the language, moving to the end of the story could be moving left or moving right. 

For more information, see <a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a> and <a href="https://msdn.microsoft.com/e1f22fc3-f8b8-465e-9684-94ddd2875be2">ITextRange::Move</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<a href="https://msdn.microsoft.com/e1f22fc3-f8b8-465e-9684-94ddd2875be2">Move</a>



<a href="https://msdn.microsoft.com/681140a4-a5c1-4992-8b81-c7d6bf2f75ea">MoveEnd</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 


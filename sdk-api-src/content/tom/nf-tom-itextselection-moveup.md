---
UID: NF:tom.ITextSelection.MoveUp
title: ITextSelection::MoveUp
author: windows-sdk-content
description: Mimics the functionality of the Up Arrow and Page Up keys.
old-location: controls\ITextSelection_MoveUp.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\moveup.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ITextSelection interface [Windows Controls],MoveUp method, ITextSelection.MoveUp, ITextSelection::MoveUp, MoveUp, MoveUp method [Windows Controls], MoveUp method [Windows Controls],ITextSelection interface, _win32_ITextSelection_MoveUp, _win32_ITextSelection_MoveUp_cpp, controls.ITextSelection_MoveUp, controls._win32_ITextSelection_MoveUp, tom/ITextSelection::MoveUp
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
 - ITextSelection.MoveUp
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextSelection::MoveUp


## -description


Mimics the functionality of the  Up Arrow and Page Up keys. 


## -parameters




### -param Unit

Type: <b>long</b>

Unit to use in the operation. It can be one of the following. 
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Corresponding key combination</th>
<th>Meaning</th>
</tr>
<tr>
<td><b>tomLine</b></td>
<td>Up Arrow</td>
<td>Moves up one line. This is the default.</td>
</tr>
<tr>
<td><b>tomParagraph</b></td>
<td>Ctrl+Up Arrow</td>
<td>Moves up one paragraph.</td>
</tr>
<tr>
<td><b>tomScreen</b></td>
<td>Page Up</td>
<td>Moves up one screen.</td>
</tr>
<tr>
<td><b>tomWindow</b></td>
<td>Ctrl+Page Up</td>
<td>Moves to first character in window.</td>
</tr>
</table>
 


### -param Count

Type: <b>long</b>

Number of <i>Units</i> to move past. The default value is 1.


### -param Extend

Type: <b>long</b>

Flag that indicates how to change the selection. If 
					<i>Extend</i> is zero (or <b>tomMove</b>), the method collapses the selection to an insertion point and then moves. If <i>Extend</i> is 1 (or <b>tomExtend</b>), the method moves the active end and leaves the other end alone. The default value is zero. A nonzero <i>Extend</i> value corresponds to the Shift key being pressed in addition to the key combination described in 
<i>Unit</i>. 


### -param pDelta

Type: <b>long*</b>

The actual count of units the insertion point or active end is moved down. This parameter can be null. Collapsing the selection counts as one unit. 


## -returns



Type: <b>HRESULT</b>

The method returns an 
						<b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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
Unit is not valid.

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



The <b>MoveUp</b> and <a href="https://msdn.microsoft.com/library/Bb774066(v=VS.85).aspx">MoveDown</a> methods are similar to the <a href="https://msdn.microsoft.com/library/Bb774074(v=VS.85).aspx">MoveLeft</a> and <a href="https://msdn.microsoft.com/library/Bb774076(v=VS.85).aspx">MoveRight</a> methods, except that they reflect the behavior of the Up Arrow, Down Arrow, Page Up, and Page Down keys on the cursor-keypad. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/Bb774060(v=VS.85).aspx">ITextSelection</a>



<a href="https://msdn.microsoft.com/library/Bb774066(v=VS.85).aspx">MoveDown</a>



<a href="https://msdn.microsoft.com/library/Bb774074(v=VS.85).aspx">MoveLeft</a>



<a href="https://msdn.microsoft.com/library/Bb774076(v=VS.85).aspx">MoveRight</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 


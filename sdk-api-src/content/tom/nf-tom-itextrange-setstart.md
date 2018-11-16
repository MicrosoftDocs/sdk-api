---
UID: NF:tom.ITextRange.SetStart
title: ITextRange::SetStart
author: windows-sdk-content
description: Sets the character position for the start of this range.
old-location: controls\ITextRange_SetStart.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setstart.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITextRange interface [Windows Controls],SetStart method, ITextRange.SetStart, ITextRange::SetStart, SetStart, SetStart method [Windows Controls], SetStart method [Windows Controls],ITextRange interface, _win32_ITextRange_SetStart, _win32_ITextRange_SetStart_cpp, controls.ITextRange_SetStart, controls._win32_ITextRange_SetStart, tom/ITextRange::SetStart
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
 - ITextRange.SetStart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tom.h
: 
- ITextRange.SetStart
: 
---

# ITextRange::SetStart


## -description


Sets the character  position for the start of this range.


## -parameters




### -param cpFirst [in]

Type: <b>long</b>

The new character position for the start of the range. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns S_FALSE.




## -remarks



Note that if <i>cpFirst</i> is greater than the range's end position, this method sets the end position equal to <i>cpFirst</i>, making the range an insertion point. If this range is the selection, the start position becomes the active end and is scrolled into view if the display isn't frozen.


<a href="https://msdn.microsoft.com/en-us/library/Bb774139(v=VS.85).aspx">ITextRange::SetEnd</a> sets the range's end position, and <a href="https://msdn.microsoft.com/en-us/library/Bb787805(v=VS.85).aspx">ITextRange::SetRange</a> sets both range ends simultaneously. The following example shows how to convert a nondegenerate range into a degenerate one (insertion point).

<code>range.End = range.Start</code>

Similarly, <code>range.Start = range.End</code> converts the range into an insertion point at the end position.

The following example adds 1 to the end position, if it is not at the end of the story.

<code>range.End = range.End + 1</code>

This also makes the end position the active end of the range, and it can turn a degenerate range into a nondegenerate one. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774026(v=VS.85).aspx">GetStart</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774058(v=VS.85).aspx">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774139(v=VS.85).aspx">SetEnd</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787805(v=VS.85).aspx">SetRange</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 


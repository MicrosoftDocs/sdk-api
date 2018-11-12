---
UID: NF:tom.ITextRange.SetEnd
title: ITextRange::SetEnd
author: windows-sdk-content
description: Sets the end position of the range.
old-location: controls\ITextRange_SetEnd.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setend.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ITextRange interface [Windows Controls],SetEnd method, ITextRange.SetEnd, ITextRange::SetEnd, SetEnd, SetEnd method [Windows Controls], SetEnd method [Windows Controls],ITextRange interface, _win32_ITextRange_SetEnd, _win32_ITextRange_SetEnd_cpp, controls.ITextRange_SetEnd, controls._win32_ITextRange_SetEnd, tom/ITextRange::SetEnd
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
 - ITextRange.SetEnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange::SetEnd


## -description


Sets the end position of the range.


## -parameters




### -param cpLim

TBD




#### - cp

Type: <b>long</b>

The new end position. 


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns S_FALSE. 




## -remarks



If the new end position is less than the start position, this method also sets the start position to  <i>cp</i>; that is, the range becomes an insertion point.

If this range is actually the selection, the end position becomes the active end and, if the display is not frozen, it is scrolled into view.


<a href="https://msdn.microsoft.com/146c335e-de5a-4418-a0af-51febde720eb">ITextRange::SetStart</a> sets the range's start position and <a href="https://msdn.microsoft.com/aad455a2-bcc1-45f8-b376-c9785400c248">ITextRange::SetRange</a> sets both range ends simultaneously. To convert a nondegenerate range, r, into a degenerate one (insertion point) at  the start position, use

<code>r.End = r.Start</code>

Similarly, r.Start = r.End converts r into an insertion point at the end position.

To add 1 to the end position, unless it is at the end of the story, use:

<code>r.End = r.End + 1</code>

This also makes end position the active end, and it can turn a degenerate range into a nondegenerate one. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/eed9c5f1-416d-4604-8a69-50b284454bb0">GetEnd</a>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/aad455a2-bcc1-45f8-b376-c9785400c248">SetRange</a>



<a href="https://msdn.microsoft.com/146c335e-de5a-4418-a0af-51febde720eb">SetStart</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 


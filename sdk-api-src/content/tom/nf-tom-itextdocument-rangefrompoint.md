---
UID: NF:tom.ITextDocument.RangeFromPoint
title: ITextDocument::RangeFromPoint
author: windows-sdk-content
description: Retrieves a range for the content at or nearest to the specified point on the screen.
old-location: controls\ITextDocument_RangeFromPoint.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\rangefrompoint.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ITextDocument interface [Windows Controls],RangeFromPoint method, ITextDocument.RangeFromPoint, ITextDocument::RangeFromPoint, RangeFromPoint, RangeFromPoint method [Windows Controls], RangeFromPoint method [Windows Controls],ITextDocument interface, _win32_ITextDocument_RangeFromPoint, _win32_ITextDocument_RangeFromPoint_cpp, controls.ITextDocument_RangeFromPoint, controls._win32_ITextDocument_RangeFromPoint, tom/ITextDocument::RangeFromPoint
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
 - ITextDocument.RangeFromPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument::RangeFromPoint


## -description


Retrieves a range for the content at or nearest to the specified point on the screen.


## -parameters




### -param x

Type: <b>long</b>

The horizontal coordinate of the specified point, in screen coordinates. 


### -param y

Type: <b>long</b>

The vertical coordinate of the specified point, in screen coordinates. 


### -param ppRange

Type: <b><a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>**</b>

The text range that corresponds to the specified point. 


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>
 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/67319d45-4ed3-4413-a725-8acb8666b7f3">Expand</a>



<a href="https://msdn.microsoft.com/67bb38d8-d96d-4d17-876d-4cadc39adece">GetPoint</a>



<a href="https://msdn.microsoft.com/0c3f161f-f6d3-44b9-b041-1b682d1915af">ITextDocument</a>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<a href="https://msdn.microsoft.com/beaad339-6aba-493e-92d2-d1213b1d07ea">MoveStart</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 


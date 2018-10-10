---
UID: NF:tom.ITextDocument.Range
title: ITextDocument::Range
author: windows-sdk-content
description: Retrieves a text range object for a specified range of content in the active story of the document.
old-location: controls\ITextDocument_Range.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\range.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: ITextDocument interface [Windows Controls],Range method, ITextDocument.Range, ITextDocument::Range, Range, Range method [Windows Controls], Range method [Windows Controls],ITextDocument interface, _win32_ITextDocument_Range, _win32_ITextDocument_Range_cpp, controls.ITextDocument_Range, controls._win32_ITextDocument_Range, tom/ITextDocument::Range
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
 - ITextDocument.Range
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument::Range


## -description


Retrieves a text range object for a specified range of content in the active story of the document.


## -parameters




### -param cpActive

TBD


### -param cpAnchor

TBD


### -param ppRange

Type: <b><a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>**</b>

Address of a pointer to a variable of type <a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a> that receives a pointer to the specified text range. 


#### - cpFirst

Type: <b>long</b>

The start position of new range. The default value is zero, which represents the start of the document. 


#### - cpLim

Type: <b>long</b>

The end position of new range. The default value is zero. 


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



<a href="https://msdn.microsoft.com/0c3f161f-f6d3-44b9-b041-1b682d1915af">ITextDocument</a>



<a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 


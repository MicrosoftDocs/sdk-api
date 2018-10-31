---
UID: NF:tom.ITextDocument.Redo
title: ITextDocument::Redo
author: windows-sdk-content
description: Performs a specified number of redo operations.
old-location: controls\ITextDocument_Redo.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\redo.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITextDocument interface [Windows Controls],Redo method, ITextDocument.Redo, ITextDocument::Redo, Redo, Redo method [Windows Controls], Redo method [Windows Controls],ITextDocument interface, _win32_ITextDocument_Redo, _win32_ITextDocument_Redo_cpp, controls.ITextDocument_Redo, controls._win32_ITextDocument_Redo, tom/ITextDocument::Redo
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
 - ITextDocument.Redo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument::Redo


## -description


Performs a specified number of redo operations. 


## -parameters




### -param Count

Type: <b>long</b>

The number of redo operations specified. 


### -param pCount

TBD




#### - prop

Type: <b>long*</b>

The actual count of redo operations performed. This parameter can be <b>NULL</b>. 


## -returns



Type: <b>HRESULT</b>

If the method succeeds it returns <b>S_OK</b>. If the method fails, it returns the following COM error code. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Less than <i>Count</i> redo operations were performed.

</td>
</tr>
</table>
 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/0c3f161f-f6d3-44b9-b041-1b682d1915af">ITextDocument</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>



<a href="https://msdn.microsoft.com/27faab46-e836-4090-98aa-a6cd3e5ecd22">Undo</a>
 

 


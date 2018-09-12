---
UID: NF:tom.ITextDocument.Undo
title: ITextDocument::Undo
author: windows-sdk-content
description: Performs a specified number of undo operations.
old-location: controls\ITextDocument_Undo.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\undo.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextDocument interface [Windows Controls],Undo method, ITextDocument.Undo, ITextDocument::Undo, Undo, Undo method [Windows Controls], Undo method [Windows Controls],ITextDocument interface, _win32_ITextDocument_Undo, _win32_ITextDocument_Undo_cpp, controls.ITextDocument_Undo, controls._win32_ITextDocument_Undo, tom/ITextDocument::Undo
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
 - ITextDocument.Undo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextDocument::Undo


## -description


Performs a specified number of undo operations.


## -parameters




### -param Count

Type: <b>long</b>

The specified number of undo operations. If the value of this parameter is <b>tomFalse</b>, undo processing is suspended. If this parameter is <b>tomTrue</b>, undo processing is restored. 


### -param pCount

TBD




#### - prop

Type: <b>long*</b>

The actual count of undo operations performed. This parameter can be <b>NULL</b>. 


## -returns



Type: <b>HRESULT</b>

If all of the 
						<i>Count</i> undo operations were performed, it returns <b>S_OK</b>. If the method fails, it returns <b>S_FALSE</b>, indicating that less than 
						<i>Count</i> undo operations were performed. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/0c3f161f-f6d3-44b9-b041-1b682d1915af">ITextDocument</a>



<a href="https://msdn.microsoft.com/45d8c366-a50a-4a0f-96c8-aa31629e280f">Redo</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 


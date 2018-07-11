---
UID: NF:tom.ITextDocument.New
title: ITextDocument::New
author: windows-sdk-content
description: Opens a new document.
old-location: controls\ITextDocument_New.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\new.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ITextDocument interface [Windows Controls],New method, ITextDocument.New, ITextDocument::New, New, New method [Windows Controls], New method [Windows Controls],ITextDocument interface, _win32_ITextDocument_New, _win32_ITextDocument_New_cpp, controls.ITextDocument_New, controls._win32_ITextDocument_New, tom/ITextDocument::New
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
 - ITextDocument.New
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument::New


## -description


Opens a new document. 


## -parameters






## -returns



Type: <b>HRESULT</b>

If the <b>ITextDocument::New</b> method succeeds, it returns <b>S_OK</b>.




## -remarks



If another document is open, this method saves any current changes and closes the current document before opening a new one.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/0c3f161f-f6d3-44b9-b041-1b682d1915af">ITextDocument</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 


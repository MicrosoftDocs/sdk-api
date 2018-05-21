---
UID: NF:tom.ITextDocument.Freeze
title: ITextDocument::Freeze
author: windows-driver-content
description: Increments the freeze count.
old-location: controls\ITextDocument_Freeze.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\freeze.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: Freeze, Freeze method [Windows Controls], Freeze method [Windows Controls],ITextDocument interface, ITextDocument interface [Windows Controls],Freeze method, ITextDocument.Freeze, ITextDocument::Freeze, _win32_ITextDocument_Freeze, _win32_ITextDocument_Freeze_cpp, controls.ITextDocument_Freeze, controls._win32_ITextDocument_Freeze, tom/ITextDocument::Freeze
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextDocument.Freeze
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument::Freeze


## -description


Increments the freeze count. 


## -parameters




### -param pCount






#### - pValue

Type: <b>long*</b>

The updated freeze count. 


## -returns



Type: <b>HRESULT</b>

If the <b>ITextDocument::Freeze</b> count is nonzero, it returns <b>S_OK</b>. If the <b>ITextDocument::Freeze</b> count is zero, it returns <b>FALSE</b>.




## -remarks



If the freeze count is nonzero, screen updating is disabled. This allows a sequence of editing operations to be performed without the performance loss and flicker of screen updating. To decrement the freeze count, call the <a href="https://msdn.microsoft.com/8b17e081-1d1f-460c-8176-8da1bd4ee9f1">ITextDocument::Unfreeze</a> method. 




## -see-also




<a href="https://msdn.microsoft.com/145cdaa0-b800-47da-a964-712e80287a3b">BeginEditCollection</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/0c3f161f-f6d3-44b9-b041-1b682d1915af">ITextDocument</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>



<a href="https://msdn.microsoft.com/8b17e081-1d1f-460c-8176-8da1bd4ee9f1">Unfreeze</a>
 

 


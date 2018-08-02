---
UID: NF:tom.ITextDocument.Freeze
title: ITextDocument::Freeze
author: windows-sdk-content
description: Increments the freeze count.
old-location: controls\ITextDocument_Freeze.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\freeze.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Freeze, Freeze method [Windows Controls], Freeze method [Windows Controls],ITextDocument interface, ITextDocument interface [Windows Controls],Freeze method, ITextDocument.Freeze, ITextDocument::Freeze, _win32_ITextDocument_Freeze, _win32_ITextDocument_Freeze_cpp, controls.ITextDocument_Freeze, controls._win32_ITextDocument_Freeze, tom/ITextDocument::Freeze
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
 - ITextDocument.Freeze
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



If the freeze count is nonzero, screen updating is disabled. This allows a sequence of editing operations to be performed without the performance loss and flicker of screen updating. To decrement the freeze count, call the <a href="https://msdn.microsoft.com/en-us/library/Bb787838(v=VS.85).aspx">ITextDocument::Unfreeze</a> method. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787730(v=VS.85).aspx">BeginEditCollection</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774052(v=VS.85).aspx">ITextDocument</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787838(v=VS.85).aspx">Unfreeze</a>
 

 


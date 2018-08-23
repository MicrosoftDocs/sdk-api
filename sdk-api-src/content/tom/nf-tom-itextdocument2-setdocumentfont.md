---
UID: NF:tom.ITextDocument2.SetDocumentFont
title: ITextDocument2::SetDocumentFont
author: windows-sdk-content
description: Sets the default character formatting for this instance of the Text Object Model (TOM) engine.
old-location: controls\itextdocument2_setdocumentfont.htm
old-project: controls
ms.assetid: 1fbc000a-76c2-4b80-856b-42f2e1829e93
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextDocument2 interface [Windows Controls],SetDocumentFont method, ITextDocument2.SetDocumentFont, ITextDocument2::SetDocumentFont, SetDocumentFont, SetDocumentFont method [Windows Controls], SetDocumentFont method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_setdocumentfont, tom/ITextDocument2::SetDocumentFont
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tom.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - ITextDocument2.SetDocumentFont
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument2::SetDocumentFont


## -description


Sets  the default character formatting for this instance of the Text Object Model (TOM) engine.


## -parameters




### -param pFont [in]

Type: <b><a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>*</b>

The font object that provides the default character formatting.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



You can also set the default character formatting by calling <a href="https://msdn.microsoft.com/en-us/library/Bb787865(v=VS.85).aspx">ITextFont::Reset(tomDefault)</a>.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/b028c2f6-8c8e-49f8-bf53-f4a639cb16c2">ITextDocument2::GetDocumentFont</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787865(v=VS.85).aspx">ITextFont::Reset</a>
 

 


---
UID: NF:tom.ITextDocument2.GetDocumentFont
title: ITextDocument2::GetDocumentFont method
author: windows-driver-content
description: Gets an object that provides the default character format information for this instance of the Text Object Model (TOM) engine.
old-location: controls\itextdocument2_getdocumentfont.htm
old-project: Controls
ms.assetid: b028c2f6-8c8e-49f8-bf53-f4a639cb16c2
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: GetDocumentFont method [Windows Controls], GetDocumentFont method [Windows Controls], ITextDocument2 interface, GetDocumentFont,ITextDocument2.GetDocumentFont, ITextDocument2, ITextDocument2 interface [Windows Controls], GetDocumentFont method, ITextDocument2::GetDocumentFont, controls.itextdocument2_getdocumentfont, tom/ITextDocument2::GetDocumentFont
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: 
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextDocument2.GetDocumentFont
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument2::GetDocumentFont method


## -description



Gets an object that provides the default character format information for this instance of the Text Object Model (TOM) engine.




## -parameters




### -param ppFont [out, retval]

Type: <b><a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>**</b>

The object that provides the default character format information.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/1fbc000a-76c2-4b80-856b-42f2e1829e93">ITextDocument2::SetDocumentFont</a>
 

 


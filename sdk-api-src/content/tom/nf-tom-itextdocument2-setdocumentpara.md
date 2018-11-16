---
UID: NF:tom.ITextDocument2.SetDocumentPara
title: ITextDocument2::SetDocumentPara
author: windows-sdk-content
description: Sets the default paragraph formatting for this instance of the Text Object Model (TOM) engine.
old-location: controls\itextdocument2_setdocumentpara.htm
tech.root: Controls
ms.assetid: d35d57e9-a005-48cd-a92d-381dc490d44f
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITextDocument2 interface [Windows Controls],SetDocumentPara method, ITextDocument2.SetDocumentPara, ITextDocument2::SetDocumentPara, SetDocumentPara, SetDocumentPara method [Windows Controls], SetDocumentPara method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_setdocumentpara, tom/ITextDocument2::SetDocumentPara
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
 - ITextDocument2.SetDocumentPara
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tom.h
: 
- ITextDocument2.SetDocumentPara
: 
---

# ITextDocument2::SetDocumentPara


## -description


Sets the default paragraph formatting  for this instance of the Text Object Model (TOM) engine.


## -parameters




### -param pPara [in]

Type: <b><a href="https://msdn.microsoft.com/31a0849f-c651-4178-b1ff-a4333bcde5d9">ITextPara2</a>*</b>

The paragraph object that provides the default paragraph formatting


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



You can also set the default paragraph formatting by calling <a href="https://msdn.microsoft.com/en-us/library/Bb787849(v=VS.85).aspx">ITextPara::Reset(tomDefault)</a>.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/3667587e-3cf1-4b86-82fd-2fc34d4cbeee">ITextDocument2::GetDocumentPara</a>
 

 


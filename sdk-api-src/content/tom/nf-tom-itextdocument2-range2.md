---
UID: NF:tom.ITextDocument2.Range2
title: ITextDocument2::Range2
author: windows-sdk-content
description: Retrieves a new text range for the active story of the document.
old-location: controls\itextdocument2_range2.htm
old-project: Controls
ms.assetid: e0cd3788-de0e-4b57-8f24-f0897e2b0bed
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ITextDocument2 interface [Windows Controls],Range2 method, ITextDocument2.Range2, ITextDocument2::Range2, Range2, Range2 method [Windows Controls], Range2 method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_range2, tom/ITextDocument2::Range2
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextDocument2.Range2
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument2::Range2


## -description


Retrieves a new text range for the active story of the document.


## -parameters




### -param cpActive [in]

Type: <b>long</b>

The active end of the new text range. The default value is 0; that is, the beginning of the story.


### -param cpAnchor [in]

Type: <b>long</b>

The anchor end of the new text range. The default value is 0.


### -param ppRange [out, retval]

Type: <b><a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>**</b>

The new text range. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>
 

 


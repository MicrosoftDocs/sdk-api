---
UID: NF:tom.ITextDocument2.SetMathProperties
title: ITextDocument2::SetMathProperties
author: windows-driver-content
description: Specifies the math properties to use for the document.
old-location: controls\itextdocument2_setmathproperties.htm
old-project: Controls
ms.assetid: a688354b-b231-44fc-9cfb-32c8e8b1361f
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ITextDocument2 interface [Windows Controls],SetMathProperties method, ITextDocument2.SetMathProperties, ITextDocument2::SetMathProperties, SetMathProperties, SetMathProperties method [Windows Controls], SetMathProperties method [Windows Controls],ITextDocument2 interface, controls.itextdocument2_setmathproperties, tom/ITextDocument2::SetMathProperties
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
-	ITextDocument2.SetMathProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument2::SetMathProperties


## -description


Specifies the math properties to use for the document.


## -parameters




### -param Options [in]

Type: <b>long</b>

The math properties to set. For a list of possible properties, see <a href="https://msdn.microsoft.com/7686d0d6-5f49-4ab6-8a9e-1e53447ffe27">GetMathProperties</a>.


### -param Mask [in]

Type: <b>long</b>

The math mask. For a list of possible masks, see <a href="https://msdn.microsoft.com/7686d0d6-5f49-4ab6-8a9e-1e53447ffe27">GetMathProperties</a>



## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/7686d0d6-5f49-4ab6-8a9e-1e53447ffe27">ITextDocument2::GetMathProperties</a>
 

 


---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 


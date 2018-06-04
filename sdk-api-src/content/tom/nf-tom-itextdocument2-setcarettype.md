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

# ITextDocument2::SetCaretType


## -description


Sets the caret type.


## -parameters




### -param Value [in]

Type: <b>long</b>

The new caret type. It can be one of the following values:

<a id="tomKoreanBlockCaret"></a>
<a id="tomkoreanblockcaret"></a>
<a id="TOMKOREANBLOCKCARET"></a>


#### tomKoreanBlockCaret

<a id="tomNormalCaret"></a>
<a id="tomnormalcaret"></a>
<a id="TOMNORMALCARET"></a>


#### tomNormalCaret

<a id="tomNullCaret"></a>
<a id="tomnullcaret"></a>
<a id="TOMNULLCARET"></a>


#### tomNullCaret


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>



<a href="https://msdn.microsoft.com/4ab170d2-50a3-4fbf-8e02-92b031bc1e4f">ITextDocument2::GetCaretType</a>
 

 


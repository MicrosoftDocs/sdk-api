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

# DeleteFont macro


## -description



The <b>DeleteFont</b> macro deletes a font object, freeing all system resources associated with the font object.




## -parameters




### -param hfont

A handle to the font object.


## -remarks



After the font object is deleted, the specified handle is no longer valid.

The <b>DeleteFont</b> macro is equivalent to calling <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> as follows:

<pre class="syntax" xml:space="preserve"><code>
   DeleteObject((HGDIOBJ)(HFONT)(hfont))
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/e7c145aa-566d-4754-a4dd-a5e71e188258">SelectFont</a>
 

 


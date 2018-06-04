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

# CreatePenIndirect function


## -description


The <b>CreatePenIndirect</b> function creates a logical cosmetic pen that has the style, width, and color specified in a structure.


## -parameters




### -param plpen

TBD




#### - lplgpn [in]

Pointer to a <a href="https://msdn.microsoft.com/0e098b5a-e249-43ad-a6d8-2509b6562453">LOGPEN</a> structure that specifies the pen's style, width, and color.


## -returns



If the function succeeds, the return value is a handle that identifies a logical cosmetic pen.

If the function fails, the return value is <b>NULL</b>.




## -remarks



After an application creates a logical pen, it can select that pen into a device context by calling the <a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a> function. After a pen is selected into a device context, it can be used to draw lines and curves.

When you no longer need the pen, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.




## -see-also




<a href="https://msdn.microsoft.com/882facd2-7e06-48f6-82e4-f20e4d5adc92">CreatePen</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a>



<a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a>



<a href="https://msdn.microsoft.com/0e098b5a-e249-43ad-a6d8-2509b6562453">LOGPEN</a>



<a href="https://msdn.microsoft.com/d5cc81b5-0df4-4ec2-8941-d63819a8d5ff">Pen Functions</a>



<a href="https://msdn.microsoft.com/624c3ea6-6e42-4577-9228-961501633937">Pens Overview</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>
 

 


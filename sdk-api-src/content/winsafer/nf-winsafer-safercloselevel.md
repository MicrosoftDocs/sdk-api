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

# SaferCloseLevel function


## -description


The <b>SaferCloseLevel</b> function closes a SAFER_LEVEL_HANDLE that was opened by using the  
<a href="https://msdn.microsoft.com/f82c4f40-5c37-4f97-95a2-4b2cc26bf41e">SaferIdentifyLevel</a> function or 
the <a href="https://msdn.microsoft.com/7deb1365-5355-4983-900b-8e4fed009403">SaferCreateLevel</a> function.


## -parameters




### -param hLevelHandle [in]

The SAFER_LEVEL_HANDLE to be closed.


## -returns



<b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




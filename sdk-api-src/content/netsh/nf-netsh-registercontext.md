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

# RegisterContext function


## -description


The 
<b>RegisterContext</b> function registers a helper context with NetShell. The 
<b>RegisterContext</b> function should be called from the 
<a href="https://msdn.microsoft.com/0060feb9-3072-4a1c-9d25-4c304f60d42d">NS_HELPER_START_FN</a> entry point (the start function) passed to the 
<a href="https://msdn.microsoft.com/9c9ac64a-6edd-4348-80c7-4192726e5108">RegisterHelper</a> function in the <b>pfnStart</b> member of the 
<a href="https://msdn.microsoft.com/5041801d-384d-4faf-b0df-2a76b083facd">NS_CONTEXT_ATTRIBUTES</a> structure passed in its <i>pChildAttributes</i> parameter.


## -parameters




### -param pChildContext [in]

Attributes of the context to register.


## -remarks



For top-level helpers, the 
<b>RegisterContext</b> parameter passed during the course of its initialization function is a pointer to the 
<b>RegisterContext</b> function. The pointer should be cast to type <b>NS_REGISTER_CONTEXT</b> before use.




## -see-also




<a href="https://msdn.microsoft.com/5041801d-384d-4faf-b0df-2a76b083facd">NS_CONTEXT_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/0060feb9-3072-4a1c-9d25-4c304f60d42d">NS_HELPER_START_FN</a>



<a href="https://msdn.microsoft.com/9c9ac64a-6edd-4348-80c7-4192726e5108">RegisterHelper</a>
 

 


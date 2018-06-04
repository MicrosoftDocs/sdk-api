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

# RegisterHelper function


## -description


The 
<b>RegisterHelper</b> function is called from within a helper's exposed 
<a href="https://msdn.microsoft.com/9af7e818-bb08-4d35-bab4-43cb94845f25">InitHelperDll</a> function, and registers the helper with the NetShell context.


## -parameters




### -param pguidParentContext [in]

A pointer to GUID of another helper under which the helper should be installed. If null, the helper is installed as a top-level helper.


### -param pfnRegisterSubContext [in]

Attributes of the helper.


## -see-also




<a href="https://msdn.microsoft.com/9af7e818-bb08-4d35-bab4-43cb94845f25">InitHelperDll</a>



<a href="https://msdn.microsoft.com/52cebe62-d4b6-4229-8418-c0ae9849822b">RegisterContext</a>
 

 


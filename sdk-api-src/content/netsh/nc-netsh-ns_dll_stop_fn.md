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

# NS_DLL_STOP_FN callback function


## -description


The 
<b>NS_DLL_STOP_FN</b> command is the DLL stop function for helper DLLs. The DLL stop function provides an opportunity for helper DLLs to release any resources before being unloaded, and is registered in the 
<a href="https://msdn.microsoft.com/52cebe62-d4b6-4229-8418-c0ae9849822b">RegisterContext</a> function. The following is an example of a DLL stop function. Be aware that <b>SampleStop</b> is a placeholder for the application-defined function name.


## -parameters




### -param dwReserved [in]

Reserved.


## -returns



Returns NO_ERROR upon success. Any other return value indicates an error.




## -remarks



The DLL stop function is called once for each helper DLL being unloaded.




## -see-also




<a href="https://msdn.microsoft.com/b2a3ae40-4aaa-41b2-965c-1467a07ab2de">NS_HELPER_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/0060feb9-3072-4a1c-9d25-4c304f60d42d">NS_HELPER_START_FN</a>



<a href="https://msdn.microsoft.com/a56c11e6-5314-43eb-9960-55987395112f">NS_HELPER_STOP_FN</a>



<a href="https://msdn.microsoft.com/52cebe62-d4b6-4229-8418-c0ae9849822b">RegisterContext</a>
 

 


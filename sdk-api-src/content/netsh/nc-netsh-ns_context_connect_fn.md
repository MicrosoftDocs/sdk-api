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

# NS_CONTEXT_CONNECT_FN callback function


## -description


The 
<b>NS_CONTEXT_CONNECT_FN</b> command is the connect function for helpers. Helpers expose a connect function that enables NetShell to connect to the helper. NetShell calls a helper connect function before calling other helper functions.

The connect function is registered with NetShell using the 
<a href="https://msdn.microsoft.com/52cebe62-d4b6-4229-8418-c0ae9849822b">RegisterContext</a> function. The following is an example of a connect function. Be aware that <b>SampleConnect</b> is a placeholder for the application-defined function name.


## -parameters




### -param pwszMachine [in]

The computer on which to perform the command, or null if the command applies to the local computer. The default value is null.


## -returns



Returns NO_ERROR upon success. Any other return value indicates an error.




## -remarks



A helper connect function is called by NetShell before NetShell calls the context dump function, if one exists, and before any command function. Two operations should be carried out during a connect function call.

If the context is remotable, specified by absence of the CMD_FLAG_LOCAL flag, the connect function should accept the computer name on which the function should operate next, and attempt to validate its ability to communicate with that computer.

If the context commands are dynamic, the context should call 
<a href="https://msdn.microsoft.com/52cebe62-d4b6-4229-8418-c0ae9849822b">RegisterContext</a> again with its latest set of commands.

Each helper is responsible for maintaining its own connection to remote computers. If access is not possible, a helper should display an appropriate error message, and must fail on the connect function.




## -see-also




<a href="https://msdn.microsoft.com/b2a3ae40-4aaa-41b2-965c-1467a07ab2de">NS_HELPER_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/61dfa4ae-cf70-4858-be10-f77a318eaa28">NetShell Flags</a>



<a href="https://msdn.microsoft.com/52cebe62-d4b6-4229-8418-c0ae9849822b">RegisterContext</a>
 

 


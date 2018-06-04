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

# FN_HANDLE_CMD callback function


## -description


The 
<b>FN_HANDLE_CMD</b> command is the command function for helpers. Helpers expose commands through the <i>pTopCmds</i> and <i>pCmdGroups</i> parameters in the 
<a href="https://msdn.microsoft.com/52cebe62-d4b6-4229-8418-c0ae9849822b">RegisterContext</a> function. The following is an example of a command function. Be aware  that <b>SampleCommand</b> is a placeholder for the application-defined function name.


## -parameters




### -param pwszMachine [in]

The name of the computer on which to perform the command, or null if the command applies to the local computer. The default value is null. 




If the context uses a connect function, this argument can be ignored.


### -param *ppwcArguments [in]

A set of command tokens.


### -param dwCurrentIndex [in]

The current index into <i>ppwcArguments</i> of the last token processed before the function was called.


### -param dwArgCount [in]

The number of arguments in the <i>ppwcArguments</i> parameter.


### -param dwFlags [in]

The command flags that pertain to the current state.


### -param pvData [in]

A data pointer. Value is null unless changed by a parent context <b>SubEntry</b> function.


### -param *pbDone [out]

A set <i>pbDone</i> to <b>TRUE</b> before returning to instruct NetShell to terminate after the command function completes. The <i>pbDone</i> parameter is set to <b>FALSE</b> by default.


## -returns



Returns NO_ERROR upon success. Any other return value indicates an error.




## -remarks



The computer name specified in <i>pwszMachine</i> is passed to each function, so a connect function is not required, as would be the case if a helper has only one command. Helpers with multiple commands can create remotability code in the connect function, rather than duplicating it in each command function.




## -see-also




<a href="https://msdn.microsoft.com/b2a3ae40-4aaa-41b2-965c-1467a07ab2de">NS_HELPER_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/52cebe62-d4b6-4229-8418-c0ae9849822b">RegisterContext</a>
 

 


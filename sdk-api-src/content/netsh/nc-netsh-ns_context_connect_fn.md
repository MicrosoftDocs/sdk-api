---
UID: NC:netsh.NS_CONTEXT_CONNECT_FN
title: NS_CONTEXT_CONNECT_FN
author: windows-driver-content
description: Is the connect function for helpers.
old-location: netshell\ns_context_connect_fn.htm
old-project: NetShell
ms.assetid: bbdc4a1c-4deb-44d0-bd87-0f3fce4d9883
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: NS_CONTEXT_CONNECT_FN, NS_CONTEXT_CONNECT_FN callback, NS_CONTEXT_CONNECT_FN callback function [NetShell], SampleConnect, _netsh_ns_context_connect_fn, netsh/NS_CONTEXT_CONNECT_FN, netshell.ns_context_connect_fn
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: netsh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NLM_USAGE_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Netsh.h
api_name:
-	NS_CONTEXT_CONNECT_FN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 


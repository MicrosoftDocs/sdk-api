---
UID: NC:netsh.NS_DLL_STOP_FN
title: NS_DLL_STOP_FN
author: windows-sdk-content
description: Is the DLL stop function for helper DLLs.
old-location: netshell\ns_dll_stop_fn.htm
old-project: NetShell
ms.assetid: 3bc6811c-0661-4fd7-aab1-6b0b21ab16f4
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: NS_DLL_STOP_FN, NS_DLL_STOP_FN callback, NS_DLL_STOP_FN callback function [NetShell], SampleStop, _netsh_ns_dll_stop_fn, netsh/NS_DLL_STOP_FN, netshell.ns_dll_stop_fn
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: NLM_USAGE_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Netsh.h
api_name:
-	NS_DLL_STOP_FN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 


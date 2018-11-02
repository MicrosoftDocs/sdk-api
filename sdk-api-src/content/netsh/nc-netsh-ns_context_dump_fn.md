---
UID: NC:netsh.NS_CONTEXT_DUMP_FN
title: NS_CONTEXT_DUMP_FN
author: windows-sdk-content
description: Is the dump function for helpers.
old-location: netshell\ns_context_dump_fn.htm
tech.root: netshell
ms.assetid: 4833c65d-1de3-4a02-9489-6e82a6145e28
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: NS_CONTEXT_DUMP_FN, NS_CONTEXT_DUMP_FN callback, NS_CONTEXT_DUMP_FN callback function [NetShell], _netsh_ns_context_dump_fn, netsh/NS_CONTEXT_DUMP_FN, netshell.ns_context_dump_fn
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Netsh.h
api_name:
 - NS_CONTEXT_DUMP_FN
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NS_CONTEXT_DUMP_FN callback function


## -description


The <b>NS_CONTEXT_DUMP_FN</b> command 
    is the dump function for helpers. The dump function is used to print comments, and is 
    registered in the <a href="https://msdn.microsoft.com/52cebe62-d4b6-4229-8418-c0ae9849822b">RegisterContext</a> function. The 
    following is an example of a dump function. Be aware that <b>SampleDump</b> is a 
    placeholder for the application-defined function name.


## -parameters




### -param pwszRouter [in]

The computer on which to perform the command, or null if the command applies to the local computer. The 
      default value is null.


### -param *ppwcArguments [in]

An array of command arguments. <i>ppwcArguments</i>[0] equates to "dump".


### -param dwArgCount [in]

The number of elements in <i>ppwcArguments</i>.


### -param pvData [in]

A pointer to an arbitrary buffer of data specified by the parent context.


## -returns



Returns NO_ERROR upon success. Any other return value indicates an error.




## -remarks



When the dump function is called, helpers should print any comments, localized, followed by a 
    <b>pushd …</b> command to enter the helper context, followed by any context-specific 
    commands, and ending with a <b>popd</b> command. More localized comments can be added thereafter, if 
    desired.




## -see-also




<a href="https://msdn.microsoft.com/b2a3ae40-4aaa-41b2-965c-1467a07ab2de">NS_HELPER_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/52cebe62-d4b6-4229-8418-c0ae9849822b">RegisterContext</a>
 

 


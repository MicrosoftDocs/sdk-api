---
UID: NC:netsh.NS_CONTEXT_CONNECT_FN
title: NS_CONTEXT_CONNECT_FN (netsh.h)
description: Is the connect function for helpers.
helpviewer_keywords: ["NS_CONTEXT_CONNECT_FN","NS_CONTEXT_CONNECT_FN callback","NS_CONTEXT_CONNECT_FN callback function [NetShell]","SampleConnect","_netsh_ns_context_connect_fn","netsh/NS_CONTEXT_CONNECT_FN","netshell.ns_context_connect_fn"]
old-location: netshell\ns_context_connect_fn.htm
tech.root: netshell
ms.assetid: bbdc4a1c-4deb-44d0-bd87-0f3fce4d9883
ms.date: 12/05/2018
ms.keywords: NS_CONTEXT_CONNECT_FN, NS_CONTEXT_CONNECT_FN callback, NS_CONTEXT_CONNECT_FN callback function [NetShell], SampleConnect, _netsh_ns_context_connect_fn, netsh/NS_CONTEXT_CONNECT_FN, netshell.ns_context_connect_fn
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NS_CONTEXT_CONNECT_FN
 - netsh/NS_CONTEXT_CONNECT_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Netsh.h
api_name:
 - NS_CONTEXT_CONNECT_FN
---

# NS_CONTEXT_CONNECT_FN callback function


## -description

The 
<b>NS_CONTEXT_CONNECT_FN</b> command is the connect function for helpers. Helpers expose a connect function that enables NetShell to connect to the helper. NetShell calls a helper connect function before calling other helper functions.

The connect function is registered with NetShell using the 
<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-registercontext">RegisterContext</a> function. The following is an example of a connect function. Be aware that <b>SampleConnect</b> is a placeholder for the application-defined function name.

## -parameters

### -param pwszMachine [in]

The computer on which to perform the command, or null if the command applies to the local computer. The default value is null.

## -returns

Returns NO_ERROR upon success. Any other return value indicates an error.

## -remarks

A helper connect function is called by NetShell before NetShell calls the context dump function, if one exists, and before any command function. Two operations should be carried out during a connect function call.

If the context is remotable, specified by absence of the CMD_FLAG_LOCAL flag, the connect function should accept the computer name on which the function should operate next, and attempt to validate its ability to communicate with that computer.

If the context commands are dynamic, the context should call 
<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-registercontext">RegisterContext</a> again with its latest set of commands.

Each helper is responsible for maintaining its own connection to remote computers. If access is not possible, a helper should display an appropriate error message, and must fail on the connect function.

## -see-also

<a href="/windows/desktop/api/netsh/ns-netsh-ns_helper_attributes">NS_HELPER_ATTRIBUTES</a>



<a href="/previous-versions/windows/desktop/netshell/netshell-flags">NetShell Flags</a>



<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-registercontext">RegisterContext</a>
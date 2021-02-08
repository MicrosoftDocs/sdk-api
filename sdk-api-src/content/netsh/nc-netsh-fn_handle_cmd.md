---
UID: NC:netsh.FN_HANDLE_CMD
title: FN_HANDLE_CMD (netsh.h)
description: Is the command function for helpers.
helpviewer_keywords: ["FN_HANDLE_CMD","FN_HANDLE_CMD callback","FN_HANDLE_CMD callback function [NetShell]","SampleCommand","_netsh_fn_handle_cmd","netsh/FN_HANDLE_CMD","netshell.fn_handle_cmd"]
old-location: netshell\fn_handle_cmd.htm
tech.root: netshell
ms.assetid: 5058e202-9ad4-4789-97db-3c13b4a1c337
ms.date: 12/05/2018
ms.keywords: FN_HANDLE_CMD, FN_HANDLE_CMD callback, FN_HANDLE_CMD callback function [NetShell], SampleCommand, _netsh_fn_handle_cmd, netsh/FN_HANDLE_CMD, netshell.fn_handle_cmd
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
 - FN_HANDLE_CMD
 - netsh/FN_HANDLE_CMD
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
 - FN_HANDLE_CMD
---

# FN_HANDLE_CMD callback function


## -description

The 
<b>FN_HANDLE_CMD</b> command is the command function for helpers. Helpers expose commands through the <i>pTopCmds</i> and <i>pCmdGroups</i> parameters in the 
<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-registercontext">RegisterContext</a> function. The following is an example of a command function. Be aware  that <b>SampleCommand</b> is a placeholder for the application-defined function name.

## -parameters

### -param pwszMachine [in]

The name of the computer on which to perform the command, or null if the command applies to the local computer. The default value is null. 




If the context uses a connect function, this argument can be ignored.

### -param ppwcArguments [in]

A set of command tokens.

### -param dwCurrentIndex [in]

The current index into <i>ppwcArguments</i> of the last token processed before the function was called.

### -param dwArgCount [in]

The number of arguments in the <i>ppwcArguments</i> parameter.

### -param dwFlags [in]

The command flags that pertain to the current state.

### -param pvData [in]

A data pointer. Value is null unless changed by a parent context <b>SubEntry</b> function.

### -param pbDone [out]

A set <i>pbDone</i> to <b>TRUE</b> before returning to instruct NetShell to terminate after the command function completes. The <i>pbDone</i> parameter is set to <b>FALSE</b> by default.

## -returns

Returns NO_ERROR upon success. Any other return value indicates an error.

## -remarks

The computer name specified in <i>pwszMachine</i> is passed to each function, so a connect function is not required, as would be the case if a helper has only one command. Helpers with multiple commands can create remotability code in the connect function, rather than duplicating it in each command function.

## -see-also

<a href="/windows/desktop/api/netsh/ns-netsh-ns_helper_attributes">NS_HELPER_ATTRIBUTES</a>



<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-registercontext">RegisterContext</a>

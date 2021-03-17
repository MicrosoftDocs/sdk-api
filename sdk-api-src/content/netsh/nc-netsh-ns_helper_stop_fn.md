---
UID: NC:netsh.NS_HELPER_STOP_FN
title: NS_HELPER_STOP_FN (netsh.h)
description: Is the stop function for helpers.
helpviewer_keywords: ["NS_HELPER_STOP_FN","NS_HELPER_STOP_FN callback","NS_HELPER_STOP_FN callback function [NetShell]","SampleStopHelper","_netsh_ns_helper_stop_fn","netsh/NS_HELPER_STOP_FN","netshell.ns_helper_stop_fn"]
old-location: netshell\ns_helper_stop_fn.htm
tech.root: netshell
ms.assetid: a56c11e6-5314-43eb-9960-55987395112f
ms.date: 12/05/2018
ms.keywords: NS_HELPER_STOP_FN, NS_HELPER_STOP_FN callback, NS_HELPER_STOP_FN callback function [NetShell], SampleStopHelper, _netsh_ns_helper_stop_fn, netsh/NS_HELPER_STOP_FN, netshell.ns_helper_stop_fn
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
 - NS_HELPER_STOP_FN
 - netsh/NS_HELPER_STOP_FN
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
 - NS_HELPER_STOP_FN
---

# NS_HELPER_STOP_FN callback function


## -description

The 
<b>NS_HELPER_STOP_FN</b> command is the stop function for helpers. This function enables helper contexts to release any resources before being unloaded, and is registered in the 
<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-registercontext">RegisterContext</a> function. The following is an example of a stop function. Be aware that <b>SampleStopHelper</b> is a placeholder for the application-defined function name.

## -parameters

### -param dwReserved [in]

Reserved.

## -returns

Returns NO_ERROR upon success. Any other return value indicates an error.

## -remarks

The stop function for helpers provides an opportunity for a helper context to release resources before being unloaded. This function is called once for each context for which the function is registered.

## -see-also

<a href="/windows/desktop/api/netsh/ns-netsh-ns_helper_attributes">NS_HELPER_ATTRIBUTES</a>



<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_helper_start_fn">NS_HELPER_START_FN</a>



<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-registercontext">RegisterContext</a>
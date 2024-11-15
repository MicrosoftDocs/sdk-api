---
UID: NC:netsh.NS_HELPER_START_FN
title: NS_HELPER_START_FN (netsh.h)
description: Is the start function for helpers.
helpviewer_keywords: ["NS_HELPER_START_FN","NS_HELPER_START_FN callback","NS_HELPER_START_FN callback function [NetShell]","_netsh_ns_helper_start_fn","netsh/NS_HELPER_START_FN","netshell.ns_helper_start_fn"]
old-location: netshell\ns_helper_start_fn.htm
tech.root: netshell
ms.assetid: 0060feb9-3072-4a1c-9d25-4c304f60d42d
ms.date: 12/05/2018
ms.keywords: NS_HELPER_START_FN, NS_HELPER_START_FN callback, NS_HELPER_START_FN callback function [NetShell], _netsh_ns_helper_start_fn, netsh/NS_HELPER_START_FN, netshell.ns_helper_start_fn
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
 - NS_HELPER_START_FN
 - netsh/NS_HELPER_START_FN
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
 - NS_HELPER_START_FN
---

# NS_HELPER_START_FN callback function


## -description

The 
<b>NS_HELPER_START_FN</b> command is the start function for helpers. The start function provides an opportunity for helpers to register contexts and is registered in the 
<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-registercontext">RegisterContext</a> function. The following is an example of a start function. Be aware that <b>SampleStartHelper</b> is a placeholder for the application-defined function name.

## -parameters

### -param pguidParent [in]

The parent under which the helper DLL should be registered.

### -param dwVersion [in]

The version of the parent helper DLL.

## -returns

Returns NO_ERROR upon success. Any other return value indicates an error.

## -remarks

A typical implementation of the start function is as follows:


``` syntax
DWORD WINAPI SampleStartHelper(
    CONST GUID *pguidParent,
    DWORD       dwVersion
)
{
    DWORD dwErr;
    NS_CONTEXT_ATTRIBUTES attMyAttributes;

    ZeroMemory(&attMyAttributes, sizeof(attMyAttributes));
    attMyAttributes.pwszContext   = L"samplecontext";
    attMyAttributes.guidHelper    = g_SampleGuid;
    attMyAttributes.dwVersion     = 1;
    attMyAttributes.dwFlags       = 0;
    attMyAttributes.ulNumTopCmds  = g_ulSampleNumTopCmds;
    attMyAttributes.pTopCmds      = (CMD_ENTRY (*)[])&g_SampleTopCmds;
    attMyAttributes.ulNumGroups   = g_ulSampleCmdGroups; 
    attMyAttributes.pCmdGroups    = (CMD_GROUP_ENTRY (*)[])&g_SampleCmdsGroups;
    attMyAttributes.pfnCommitFn   = SampleCommit;
    attMyAttributes.pfnDumpFn     = SampleDump;
    attMyAttributes.pfnConnectFn  = SampleConnect;

    dwErr = RegisterContext( &attMyAttributes );
    return dwErr;
}
```


## -see-also

<a href="/windows/desktop/api/netsh/ns-netsh-ns_helper_attributes">NS_HELPER_ATTRIBUTES</a>



<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_helper_stop_fn">NS_HELPER_STOP_FN</a>



<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-registercontext">RegisterContext</a>

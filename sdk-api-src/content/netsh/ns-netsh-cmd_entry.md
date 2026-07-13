---
UID: NS:netsh._CMD_ENTRY
title: CMD_ENTRY (netsh.h)
description: Defines a helper command.
helpviewer_keywords: ["*PCMD_ENTRY","CMD_ENTRY","CMD_ENTRY structure [NetShell]","PCMD_ENTRY","PCMD_ENTRY structure pointer [NetShell]","_netsh_cmd_entry","netsh/CMD_ENTRY","netsh/PCMD_ENTRY","netshell.cmd_entry"]
old-location: netshell\cmd_entry.htm
tech.root: netshell
ms.assetid: 299962c8-8f93-4b22-a232-8230eb64cc12
ms.date: 12/05/2018
ms.keywords: '*PCMD_ENTRY, CMD_ENTRY, CMD_ENTRY structure [NetShell], PCMD_ENTRY, PCMD_ENTRY structure pointer [NetShell], _netsh_cmd_entry, netsh/CMD_ENTRY, netsh/PCMD_ENTRY, netshell.cmd_entry'
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
req.typenames: CMD_ENTRY, *PCMD_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMD_ENTRY
 - netsh/_CMD_ENTRY
 - PCMD_ENTRY
 - netsh/PCMD_ENTRY
 - CMD_ENTRY
 - netsh/CMD_ENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netsh.h
api_name:
 - CMD_ENTRY
---

# CMD_ENTRY structure


## -description

The 
<b>CMD_ENTRY</b> structure defines a helper command.

## -struct-fields

### -field pwszCmdToken

The token (name) for the command.

### -field pfnCmdHandler

A function that handles the command. For more information, see 
<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-fn_handle_cmd">FN_HANDLE_CMD</a>.

### -field dwShortCmdHelpToken

A short help message. This is the message identifier from the resource file of the helper DLL.

### -field dwCmdHlpToken

The message to display if the command is followed only by a help token (HELP, /?, -?, or ?). This is the message identifier from the resource file of the helper DLL.

### -field dwFlags

The flags for the command. For more information, see 
<a href="/previous-versions/windows/desktop/netshell/netshell-flags">Netshell Flags</a>.

### -field pOsVersionCheck

The operating system version check function. This is the function used to determine whether the command can be run on the operating system running on the local and/or remote context before invoking or displaying commands. For more information, see 
<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_osversioncheck">NS_OSVERSIONCHECK</a>.

## -remarks

Macros are available that can simplify the creation of the 
<b>CMD_ENTRY</b> structure, as follows:


``` syntax
#define CREATE_CMD_ENTRY_EX(t,f,i)       {CMD_##t, f, HLP_##t, HLP_##t##_EX, i, NULL}
#define CREATE_CMD_ENTRY_EX_VER(t,f,i,v) {CMD_##t, f, HLP_##t, HLP_##t##_EX, i, v}
#define CREATE_CMD_ENTRY(t,f)            {CMD_##t, f, HLP_##t, HLP_##t##_EX, CMD_FLAG_PRIVATE, NULL}
```

If these macros are used, the following constants must be defined in the helper DLL:



The following are example uses of these macros:


```cpp
#define HLP_SAMPLE_ADD_BAR        1001
#define HLP_SAMPLE_ADD_BAR_EX     1002
#define HLP_SAMPLE_DELETE_BAR     1003
#define HLP_SAMPLE_DELETE_BAR_EX  1004
#define HLP_SAMPLE_SET_GLOBAL     1005
#define HLP_SAMPLE_SET_GLOBAL_EX  1006
#define HLP_SAMPLE_SET_BAR        1007
#define HLP_SAMPLE_SET_BAR_EX     1008
#define HLP_SAMPLE_SET_FILTER     1009
#define HLP_SAMPLE_SET_FILTER_EX  1010
#define HLP_SAMPLE_SHOW_GLOBAL    1011
#define HLP_SAMPLE_SHOW_GLOBAL_EX 1012
#define HLP_SAMPLE_SHOW_BAR       1013
#define HLP_SAMPLE_SHOW_BAR_EX    1014
#define HLP_SAMPLE_SHOW_FILTER    1015
#define HLP_SAMPLE_SHOW_FILTER_EX 1016

#define CMD_SAMPLE_ADD_BAR        L"add_bar"
#define CMD_SAMPLE_DELETE_BAR     L"delete_bar"
#define CMD_SAMPLE_SET_GLOBAL     L"set_global"
#define CMD_SAMPLE_SET_BAR        L"set_bar"
#define CMD_SAMPLE_SET_FILTER     L"set_filter"
#define CMD_SAMPLE_SHOW_GLOBAL    L"show_global"
#define CMD_SAMPLE_SHOW_BAR       L"show_bar"
#define CMD_SAMPLE_SHOW_FILTER    L"show_filter"

CMD_ENTRY  g_SampleAddCmdTable[] = 
{
    CREATE_CMD_ENTRY(SAMPLE_ADD_BAR, HandleSampleAddBar),
};
CMD_ENTRY  g_SampleDeleteCmdTable[] = 
{
    CREATE_CMD_ENTRY(SAMPLE_DELETE_BAR, HandleSampleDeleteBar),
};
CMD_ENTRY  g_SampleSetCmdTable[] = 
{
    CREATE_CMD_ENTRY(SAMPLE_SET_GLOBAL, HandleSampleSetGlobal),
    CREATE_CMD_ENTRY_EX(SAMPLE_SET_BAR, HandleSampleSetBar, (CMD_FLAG_PRIVATE | CMD_FLAG_ONLINE) ),
    CREATE_CMD_ENTRY_EX_VER(SAMPLE_SET_FILTER, HandleSampleSetFilter, (CMD_FLAG_PRIVATE | CMD_FLAG_ONLINE), CheckRunningOnWindowsXP),
};
CMD_ENTRY  g_SampleShowCmdTable[] = 
{
    CREATE_CMD_ENTRY(SAMPLE_SHOW_GLOBAL, HandleSampleShowGlobal),
    CREATE_CMD_ENTRY_EX(SAMPLE_SHOW_BAR, HandleSampleShowBar, (CMD_FLAG_PRIVATE | CMD_FLAG_ONLINE) ),
    CREATE_CMD_ENTRY_EX_VER(SAMPLE_SHOW_FILTER, HandleSampleShowFilter, (CMD_FLAG_PRIVATE | CMD_FLAG_ONLINE), CheckRunningOnWindowsXP),
};

```

## -see-also

<a href="/windows/desktop/api/netsh/ns-netsh-cmd_group_entry">CMD_GROUP_ENTRY</a>



<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_context_commit_fn">NS_CONTEXT_COMMIT_FN</a>



<a href="/previous-versions/windows/desktop/netshell/netshell-flags">NetShell Flags</a>

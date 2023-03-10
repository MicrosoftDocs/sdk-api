---
UID: NS:netsh._CMD_GROUP_ENTRY
title: CMD_GROUP_ENTRY (netsh.h)
description: Defines a group of helper commands.
helpviewer_keywords: ["*PCMD_GROUP_ENTRY","CMD_GROUP_ENTRY","CMD_GROUP_ENTRY structure [NetShell]","PCMD_GROUP_ENTRY","PCMD_GROUP_ENTRY structure pointer [NetShell]","_netsh_cmd_group_entry","netsh/CMD_GROUP_ENTRY","netsh/PCMD_GROUP_ENTRY","netshell.cmd_group_entry"]
old-location: netshell\cmd_group_entry.htm
tech.root: netshell
ms.assetid: dc0d6449-f635-417c-8363-51e61c417051
ms.date: 12/05/2018
ms.keywords: '*PCMD_GROUP_ENTRY, CMD_GROUP_ENTRY, CMD_GROUP_ENTRY structure [NetShell], PCMD_GROUP_ENTRY, PCMD_GROUP_ENTRY structure pointer [NetShell], _netsh_cmd_group_entry, netsh/CMD_GROUP_ENTRY, netsh/PCMD_GROUP_ENTRY, netshell.cmd_group_entry'
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
req.typenames: CMD_GROUP_ENTRY, *PCMD_GROUP_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CMD_GROUP_ENTRY
 - netsh/_CMD_GROUP_ENTRY
 - PCMD_GROUP_ENTRY
 - netsh/PCMD_GROUP_ENTRY
 - CMD_GROUP_ENTRY
 - netsh/CMD_GROUP_ENTRY
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
 - CMD_GROUP_ENTRY
---

# CMD_GROUP_ENTRY structure


## -description

the 
<b>CMD_GROUP_ENTRY</b> structure defines a group of helper commands.

## -struct-fields

### -field pwszCmdGroupToken

The token (name) for the command group

### -field dwShortCmdHelpToken

A short help message.

### -field ulCmdGroupSize

The number of elements in the command group.

### -field dwFlags

Flags. For more information, see 
<a href="/previous-versions/windows/desktop/netshell/netshell-flags">NetShell Flags</a>.

### -field pCmdGroup

An array of CMD_ENTRY structures.

### -field pOsVersionCheck

An operating system version check function. This is the function used to determine whether the command can be run on the operating system running on the local and/or remote context before invoking or displaying commands. For more information, see 
<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_osversioncheck">NS_OSVERSIONCHECK</a>.

## -remarks

Macros are available that can simplify the creation of the 
<b>CMD_GROUP_ENTRY</b> structure, as follows:


``` syntax
#define CREATE_CMD_GROUP_ENTRY_EX(t,s,i)       {CMD_##t, HLP_##t, sizeof(s)/sizeof(CMD_ENTRY), i, s, NULL }
#define CREATE_CMD_GROUP_ENTRY_EX_VER(t,s,i,v) {CMD_##t, HLP_##t, sizeof(s)/sizeof(CMD_ENTRY), i, s, v }
#define CREATE_CMD_GROUP_ENTRY(t,s)            {CMD_##t, HLP_##t, sizeof(s)/sizeof(CMD_ENTRY), 0, s, NULL }

```

If these macros are used, the following constants must be defined in the helper DLL:



The following are example uses of these macros:


```cpp
#define HLP_GROUP_ADD        1100
#define HLP_GROUP_ADD_EX     1101
#define HLP_GROUP_DELETE     1102
#define HLP_GROUP_DELETE_EX  1103
#define HLP_GROUP_SET        1104
#define HLP_GROUP_SET_EX     1105
#define HLP_GROUP_SHOW       1106
#define HLP_GROUP_SHOW_EX    1107

#define CMD_GROUP_ADD        L"add"
#define CMD_GROUP_DELETE     L"delete"
#define CMD_GROUP_SET        L"set"
#define CMD_GROUP_SHOW       L"show"

static CMD_GROUP_ENTRY g_SampleGroupCmds[] = 
{
    CREATE_CMD_GROUP_ENTRY(GROUP_ADD,    g_SampleAddCmdTable),
    CREATE_CMD_GROUP_ENTRY(GROUP_DELETE, g_SampleDeleteCmdTable),
    CREATE_CMD_GROUP_ENTRY(GROUP_SET,    g_SampleSetCmdTable),
    CREATE_CMD_GROUP_ENTRY(GROUP_SHOW,   g_SampleShowCmdTable),
};

```

## -see-also

<a href="/windows/desktop/api/netsh/ns-netsh-cmd_entry">CMD_ENTRY</a>



<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_context_commit_fn">NS_CONTEXT_COMMIT_FN</a>



<a href="/previous-versions/windows/desktop/netshell/netshell-flags">NetShell Flags</a>

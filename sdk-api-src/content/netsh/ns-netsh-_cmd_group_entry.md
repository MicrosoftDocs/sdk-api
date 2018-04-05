---
UID: NS:netsh._CMD_GROUP_ENTRY
title: "_CMD_GROUP_ENTRY"
author: windows-driver-content
description: Defines a group of helper commands.
old-location: netshell\cmd_group_entry.htm
old-project: NetShell
ms.assetid: dc0d6449-f635-417c-8363-51e61c417051
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: "*PCMD_GROUP_ENTRY, CMD_GROUP_ENTRY, CMD_GROUP_ENTRY structure [NetShell], PCMD_GROUP_ENTRY, PCMD_GROUP_ENTRY structure pointer [NetShell], _CMD_GROUP_ENTRY, _netsh_cmd_group_entry, netsh/CMD_GROUP_ENTRY, netsh/PCMD_GROUP_ENTRY, netshell.cmd_group_entry"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: CMD_GROUP_ENTRY, *PCMD_GROUP_ENTRY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Netsh.h
api_name:
-	CMD_GROUP_ENTRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _CMD_GROUP_ENTRY structure


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
<a href="https://msdn.microsoft.com/61dfa4ae-cf70-4858-be10-f77a318eaa28">NetShell Flags</a>.


### -field pCmdGroup

An array of CMD_ENTRY structures.


### -field pOsVersionCheck

An operating system version check function. This is the function used to determine whether the command can be run on the operating system running on the local and/or remote context before invoking or displaying commands. For more information, see 
<a href="https://msdn.microsoft.com/d58258ac-a16a-4983-bf35-71153dcbe652">NS_OSVERSIONCHECK</a>.


## -remarks



Macros are available that can simplify the creation of the 
<b>CMD_GROUP_ENTRY</b> structure, as follows:

<pre class="syntax" xml:space="preserve"><code>#define CREATE_CMD_GROUP_ENTRY_EX(t,s,i)       {CMD_##t, HLP_##t, sizeof(s)/sizeof(CMD_ENTRY), i, s, NULL }
#define CREATE_CMD_GROUP_ENTRY_EX_VER(t,s,i,v) {CMD_##t, HLP_##t, sizeof(s)/sizeof(CMD_ENTRY), i, s, v }
#define CREATE_CMD_GROUP_ENTRY(t,s)            {CMD_##t, HLP_##t, sizeof(s)/sizeof(CMD_ENTRY), 0, s, NULL }
</code></pre>
If these macros are used, the following constants must be defined in the helper DLL:



The following are example uses of these macros:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define HLP_GROUP_ADD        1100
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/299962c8-8f93-4b22-a232-8230eb64cc12">CMD_ENTRY</a>



<a href="https://msdn.microsoft.com/2380cd4e-5e41-4bfb-874c-50be09044c85">NS_CONTEXT_COMMIT_FN</a>



<a href="https://msdn.microsoft.com/61dfa4ae-cf70-4858-be10-f77a318eaa28">NetShell Flags</a>
 

 


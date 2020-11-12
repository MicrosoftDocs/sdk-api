---
UID: NS:netsh._NS_CONTEXT_ATTRIBUTES
title: NS_CONTEXT_ATTRIBUTES (netsh.h)
description: Defines attributes of a context.
helpviewer_keywords: ["*PNS_CONTEXT_ATTRIBUTES","CMD_FLAG_INTERACTIVE","CMD_FLAG_LOCAL","CMD_FLAG_ONLINE","CMD_FLAG_PRIORITY","NS_CONTEXT_ATTRIBUTES","NS_CONTEXT_ATTRIBUTES structure [NetShell]","PNS_CONTEXT_ATTRIBUTES","PNS_CONTEXT_ATTRIBUTES structure pointer [NetShell]","_netsh_ns_context_attributes","netsh/NS_CONTEXT_ATTRIBUTES","netsh/PNS_CONTEXT_ATTRIBUTES","netshell.ns_context_attributes"]
old-location: netshell\ns_context_attributes.htm
tech.root: netshell
ms.assetid: 5041801d-384d-4faf-b0df-2a76b083facd
ms.date: 12/05/2018
ms.keywords: '*PNS_CONTEXT_ATTRIBUTES, CMD_FLAG_INTERACTIVE, CMD_FLAG_LOCAL, CMD_FLAG_ONLINE, CMD_FLAG_PRIORITY, NS_CONTEXT_ATTRIBUTES, NS_CONTEXT_ATTRIBUTES structure [NetShell], PNS_CONTEXT_ATTRIBUTES, PNS_CONTEXT_ATTRIBUTES structure pointer [NetShell], _netsh_ns_context_attributes, netsh/NS_CONTEXT_ATTRIBUTES, netsh/PNS_CONTEXT_ATTRIBUTES, netshell.ns_context_attributes'
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
req.typenames: NS_CONTEXT_ATTRIBUTES, *PNS_CONTEXT_ATTRIBUTES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NS_CONTEXT_ATTRIBUTES
 - netsh/_NS_CONTEXT_ATTRIBUTES
 - PNS_CONTEXT_ATTRIBUTES
 - netsh/PNS_CONTEXT_ATTRIBUTES
 - NS_CONTEXT_ATTRIBUTES
 - netsh/NS_CONTEXT_ATTRIBUTES
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
 - NS_CONTEXT_ATTRIBUTES
---

# NS_CONTEXT_ATTRIBUTES structure


## -description

The 
<b>NS_CONTEXT_ATTRIBUTES</b> structure defines attributes of a context.

## -struct-fields

### -field dwVersion

The version of the helper.

### -field dwReserved

Reserved. Must be zero.

### -field _ullAlign

### -field pwszContext

A unicode string that identifies the new context. This string is the command available to users. The string must not contain spaces.

### -field guidHelper

A pointer to the GUID of this helper. Identical to the value passed to the 
<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-registerhelper">RegisterHelper</a> function as the <b>pguidHelper</b> member of the 
<a href="/windows/desktop/api/netsh/ns-netsh-ns_helper_attributes">NS_HELPER_ATTRIBUTES</a> structure.

### -field dwFlags

A set of flags that limit when this context is available. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CMD_FLAG_INTERACTIVE"></a><a id="cmd_flag_interactive"></a><dl>
<dt><b>CMD_FLAG_INTERACTIVE</b></dt>
</dl>
</td>
<td width="60%">
If set, context is available only when NetSh is run in interactive mode, but is not available to be passed to NetSh on the command line.

</td>
</tr>
<tr>
<td width="40%"><a id="CMD_FLAG_LOCAL"></a><a id="cmd_flag_local"></a><dl>
<dt><b>CMD_FLAG_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
If set, the context is not valid from a remote computer.

</td>
</tr>
<tr>
<td width="40%"><a id="CMD_FLAG_ONLINE"></a><a id="cmd_flag_online"></a><dl>
<dt><b>CMD_FLAG_ONLINE</b></dt>
</dl>
</td>
<td width="60%">
If set, the context is not valid in offline mode.

</td>
</tr>
<tr>
<td width="40%"><a id="CMD_FLAG_PRIORITY"></a><a id="cmd_flag_priority"></a><dl>
<dt><b>CMD_FLAG_PRIORITY</b></dt>
</dl>
</td>
<td width="60%">
If set, the ulPriority field is used.

</td>
</tr>
</table>

### -field ulPriority

A priority value used when ordering dump and commit commands. Used only when the CMD_FLAG_PRIORITY flag is set in <b>dwFlags</b>. Default value is DEFAULT_CONTEXT_PRIORITY, defined as 100 in NetSh.h. Lower values indicate higher priority.

### -field ulNumTopCmds

The number of entries in the <b>pTopCmds</b> member.

### -field pTopCmds

An array of <a href="/windows/desktop/api/netsh/ns-netsh-cmd_entry">CMD_ENTRY</a> structures that contain helper commands.


### -field _CMD_ENTRY

### -field ulNumGroups

A number of entries in the <b>pCmdGroups</b> member.

### -field pCmdGroups

An array of <a href="/windows/desktop/api/netsh/ns-netsh-cmd_group_entry">CMD_GROUP_ENTRY</a> structures that contain helper command groups.

### -field _CMD_GROUP_ENTRY

### -field pfnCommitFn

A function called to commit changes from offline mode. Can be null. For more information about the commit function, see 
<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_context_commit_fn">NS_CONTEXT_COMMIT_FN</a>.

### -field pfnDumpFn

A function called to dump the current configuration. Can be null. For more information about the dump function, see 
<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_context_dump_fn">NS_CONTEXT_DUMP_FN</a>.

### -field pfnConnectFn

A function called to connect to a remote computer, or to update the set of available commands. Can be null. For more information about the connect function, see <a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_context_connect_fn">NS_CONTEXT_CONNECT_FN</a>.

### -field pReserved

Reserved. Must be null.

### -field pfnOsVersionCheck



## -see-also

<a href="/windows/desktop/api/netsh/ns-netsh-cmd_entry">CMD_ENTRY</a>



<a href="/windows/desktop/api/netsh/ns-netsh-cmd_group_entry">CMD_GROUP_ENTRY</a>



<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_context_commit_fn">NS_CONTEXT_COMMIT_FN</a>



<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_context_connect_fn">NS_CONTEXT_CONNECT_FN</a>



<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_context_dump_fn">NS_CONTEXT_DUMP_FN</a>



<a href="/windows/desktop/api/netsh/ns-netsh-ns_helper_attributes">NS_HELPER_ATTRIBUTES</a>



<a href="/previous-versions/windows/desktop/netshell/netshell-flags">NetShell Flags</a>
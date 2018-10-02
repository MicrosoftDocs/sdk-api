---
UID: NS:netsh._NS_CONTEXT_ATTRIBUTES
title: "_NS_CONTEXT_ATTRIBUTES"
author: windows-sdk-content
description: Defines attributes of a context.
old-location: netshell\ns_context_attributes.htm
tech.root: NetShell
ms.assetid: 5041801d-384d-4faf-b0df-2a76b083facd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PNS_CONTEXT_ATTRIBUTES, CMD_FLAG_INTERACTIVE, CMD_FLAG_LOCAL, CMD_FLAG_ONLINE, CMD_FLAG_PRIORITY, NS_CONTEXT_ATTRIBUTES, NS_CONTEXT_ATTRIBUTES structure [NetShell], PNS_CONTEXT_ATTRIBUTES, PNS_CONTEXT_ATTRIBUTES structure pointer [NetShell], _NS_CONTEXT_ATTRIBUTES, _netsh_ns_context_attributes, netsh/NS_CONTEXT_ATTRIBUTES, netsh/PNS_CONTEXT_ATTRIBUTES, netshell.ns_context_attributes"
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netsh.h
api_name:
 - NS_CONTEXT_ATTRIBUTES
product: Windows
targetos: Windows
req.typenames: NS_CONTEXT_ATTRIBUTES, *PNS_CONTEXT_ATTRIBUTES
req.redist: 
---

# _NS_CONTEXT_ATTRIBUTES structure


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
<a href="https://msdn.microsoft.com/9c9ac64a-6edd-4348-80c7-4192726e5108">RegisterHelper</a> function as the <b>pguidHelper</b> member of the 
<a href="https://msdn.microsoft.com/b2a3ae40-4aaa-41b2-965c-1467a07ab2de">NS_HELPER_ATTRIBUTES</a> structure.


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

 


### -field _CMD_ENTRY

 


### -field ulNumGroups

A number of entries in the <b>pCmdGroups</b> member.


### -field pCmdGroups

 


### -field _CMD_GROUP_ENTRY

 


### -field pfnCommitFn

A function called to commit changes from offline mode. Can be null. For more information about the commit function, see 
<a href="https://msdn.microsoft.com/2380cd4e-5e41-4bfb-874c-50be09044c85">NS_CONTEXT_COMMIT_FN</a>.


### -field pfnDumpFn

A function called to dump the current configuration. Can be null. For more information about the dump function, see 
<a href="https://msdn.microsoft.com/4833c65d-1de3-4a02-9489-6e82a6145e28">NS_CONTEXT_DUMP_FN</a>.


### -field pfnConnectFn

A function called to connect to a remote computer, or to update the set of available commands. Can be null. For more information about the connect function, see <a href="https://msdn.microsoft.com/bbdc4a1c-4deb-44d0-bd87-0f3fce4d9883">NS_CONTEXT_CONNECT_FN</a>.


### -field pReserved

Reserved. Must be null.


### -field pfnOsVersionCheck

 




#### - (pCmdGroups)

An array of <a href="https://msdn.microsoft.com/dc0d6449-f635-417c-8363-51e61c417051">CMD_GROUP_ENTRY</a> structures that contain helper command groups.
					


#### - (pTopCmds)

An array of <a href="https://msdn.microsoft.com/299962c8-8f93-4b22-a232-8230eb64cc12">CMD_ENTRY</a> structures that contain helper commands.
					


## -see-also




<a href="https://msdn.microsoft.com/299962c8-8f93-4b22-a232-8230eb64cc12">CMD_ENTRY</a>



<a href="https://msdn.microsoft.com/dc0d6449-f635-417c-8363-51e61c417051">CMD_GROUP_ENTRY</a>



<a href="https://msdn.microsoft.com/2380cd4e-5e41-4bfb-874c-50be09044c85">NS_CONTEXT_COMMIT_FN</a>



<a href="https://msdn.microsoft.com/bbdc4a1c-4deb-44d0-bd87-0f3fce4d9883">NS_CONTEXT_CONNECT_FN</a>



<a href="https://msdn.microsoft.com/4833c65d-1de3-4a02-9489-6e82a6145e28">NS_CONTEXT_DUMP_FN</a>



<a href="https://msdn.microsoft.com/b2a3ae40-4aaa-41b2-965c-1467a07ab2de">NS_HELPER_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/61dfa4ae-cf70-4858-be10-f77a318eaa28">NetShell Flags</a>
 

 


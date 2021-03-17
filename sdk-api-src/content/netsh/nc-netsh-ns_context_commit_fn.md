---
UID: NC:netsh.NS_CONTEXT_COMMIT_FN
title: NS_CONTEXT_COMMIT_FN (netsh.h)
description: Is the commit function for helpers.
helpviewer_keywords: ["NETSH_COMMIT","NETSH_FLUSH","NETSH_SAVE","NETSH_UNCOMMIT","NS_CONTEXT_COMMIT_FN","NS_CONTEXT_COMMIT_FN callback","NS_CONTEXT_COMMIT_FN callback function [NetShell]","SampleCommit","_netsh_ns_context_commit_fn","netsh/NS_CONTEXT_COMMIT_FN","netshell.ns_context_commit_fn"]
old-location: netshell\ns_context_commit_fn.htm
tech.root: netshell
ms.assetid: 2380cd4e-5e41-4bfb-874c-50be09044c85
ms.date: 12/05/2018
ms.keywords: NETSH_COMMIT, NETSH_FLUSH, NETSH_SAVE, NETSH_UNCOMMIT, NS_CONTEXT_COMMIT_FN, NS_CONTEXT_COMMIT_FN callback, NS_CONTEXT_COMMIT_FN callback function [NetShell], SampleCommit, _netsh_ns_context_commit_fn, netsh/NS_CONTEXT_COMMIT_FN, netshell.ns_context_commit_fn
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
 - NS_CONTEXT_COMMIT_FN
 - netsh/NS_CONTEXT_COMMIT_FN
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
 - NS_CONTEXT_COMMIT_FN
---

# NS_CONTEXT_COMMIT_FN callback function


## -description

The 
<b>NS_CONTEXT_COMMIT_FN</b> command is the commit function for helpers. The commit function commits commands used for committing offline commands, and is registered in the 
<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-registercontext">RegisterContext</a> function. The following is an example of a commit function. Be aware  that <b>SampleCommit</b> is a placeholder for the application-defined function name.

## -parameters

### -param dwAction [in]

A value that specifies the commit action. Must be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NETSH_COMMIT"></a><a id="netsh_commit"></a><dl>
<dt><b>NETSH_COMMIT</b></dt>
</dl>
</td>
<td width="60%">
Changes to commit mode.

</td>
</tr>
<tr>
<td width="40%"><a id="NETSH_UNCOMMIT"></a><a id="netsh_uncommit"></a><dl>
<dt><b>NETSH_UNCOMMIT</b></dt>
</dl>
</td>
<td width="60%">
Changes to uncommit mode.

</td>
</tr>
<tr>
<td width="40%"><a id="NETSH_SAVE"></a><a id="netsh_save"></a><dl>
<dt><b>NETSH_SAVE</b></dt>
</dl>
</td>
<td width="60%">
Saves all uncommitted changes.

</td>
</tr>
<tr>
<td width="40%"><a id="NETSH_FLUSH"></a><a id="netsh_flush"></a><dl>
<dt><b>NETSH_FLUSH</b></dt>
</dl>
</td>
<td width="60%">
Flushes all uncommitted changes.

</td>
</tr>
</table>

## -returns

Returns NO_ERROR upon success. Any other return value indicates an error.

## -see-also

<a href="/windows/desktop/api/netsh/ns-netsh-ns_helper_attributes">NS_HELPER_ATTRIBUTES</a>



<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-registercontext">RegisterContext</a>
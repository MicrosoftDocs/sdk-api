---
UID: NF:netfw.INetFwPolicy2.RestoreLocalFirewallDefaults
title: INetFwPolicy2::RestoreLocalFirewallDefaults (netfw.h)
description: Restores the local firewall configuration to its default state.
helpviewer_keywords: ["INetFwPolicy2 interface [ICS/ICF]","RestoreLocalFirewallDefaults method","INetFwPolicy2.RestoreLocalFirewallDefaults","INetFwPolicy2::RestoreLocalFirewallDefaults","RestoreLocalFirewallDefaults","RestoreLocalFirewallDefaults method [ICS/ICF]","RestoreLocalFirewallDefaults method [ICS/ICF]","INetFwPolicy2 interface","ics.inetfwpolicy2_restorelocalfirewalldefaults","netfw/INetFwPolicy2::RestoreLocalFirewallDefaults"]
old-location: ics\inetfwpolicy2_restorelocalfirewalldefaults.htm
tech.root: ics
ms.assetid: 420b07ff-e851-41cf-96c4-064430f292a1
ms.date: 12/05/2018
ms.keywords: INetFwPolicy2 interface [ICS/ICF],RestoreLocalFirewallDefaults method, INetFwPolicy2.RestoreLocalFirewallDefaults, INetFwPolicy2::RestoreLocalFirewallDefaults, RestoreLocalFirewallDefaults, RestoreLocalFirewallDefaults method [ICS/ICF], RestoreLocalFirewallDefaults method [ICS/ICF],INetFwPolicy2 interface, ics.inetfwpolicy2_restorelocalfirewalldefaults, netfw/INetFwPolicy2::RestoreLocalFirewallDefaults
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: FirewallAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetFwPolicy2::RestoreLocalFirewallDefaults
 - netfw/INetFwPolicy2::RestoreLocalFirewallDefaults
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwPolicy2.RestoreLocalFirewallDefaults
---

# INetFwPolicy2::RestoreLocalFirewallDefaults


## -description

The <b>RestoreLocalFirewallDefaults</b> method restores the local firewall configuration to its default state.



## -returns

<h3>C++</h3>
If the method succeeds the return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted due to permissions issues.

</td>
</tr>
</table>
 

<h3>VB</h3>
If the method succeeds the return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted due to permissions issues.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2">INetFwPolicy2</a>

---
UID: NF:netfw.INetFwPolicy2.RestoreLocalFirewallDefaults
title: INetFwPolicy2::RestoreLocalFirewallDefaults
author: windows-sdk-content
description: Restores the local firewall configuration to its default state.
old-location: ics\inetfwpolicy2_restorelocalfirewalldefaults.htm
old-project: ics
ms.assetid: 420b07ff-e851-41cf-96c4-064430f292a1
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: INetFwPolicy2 interface [ICS/ICF],RestoreLocalFirewallDefaults method, INetFwPolicy2.RestoreLocalFirewallDefaults, INetFwPolicy2::RestoreLocalFirewallDefaults, RestoreLocalFirewallDefaults, RestoreLocalFirewallDefaults method [ICS/ICF], RestoreLocalFirewallDefaults method [ICS/ICF],INetFwPolicy2 interface, ics.inetfwpolicy2_restorelocalfirewalldefaults, netfw/INetFwPolicy2::RestoreLocalFirewallDefaults
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: netfw.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: NETISO_ERROR_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwPolicy2.RestoreLocalFirewallDefaults
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetFwPolicy2::RestoreLocalFirewallDefaults


## -description


The <b>RestoreLocalFirewallDefaults</b> method restores the local firewall configuration to its default state.


## -parameters






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




<a href="https://msdn.microsoft.com/ef01a531-ddb0-4eb4-894b-82f613016396">INetFwPolicy2</a>
 

 


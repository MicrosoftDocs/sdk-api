---
UID: NF:netfw.INetFwMgr.RestoreDefaults
title: INetFwMgr::RestoreDefaults (netfw.h)
description: Restores the local configuration to its default, installed state.
helpviewer_keywords: ["INetFwMgr interface [ICS/ICF]","RestoreDefaults method","INetFwMgr.RestoreDefaults","INetFwMgr::RestoreDefaults","RestoreDefaults","RestoreDefaults method [ICS/ICF]","RestoreDefaults method [ICS/ICF]","INetFwMgr interface","ics.inetfwmgr_restoredefaults","netfw/INetFwMgr::RestoreDefaults"]
old-location: ics\inetfwmgr_restoredefaults.htm
tech.root: ics
ms.assetid: ed2fd6b6-e449-4bed-aeb4-eb4345f67b12
ms.date: 12/05/2018
ms.keywords: INetFwMgr interface [ICS/ICF],RestoreDefaults method, INetFwMgr.RestoreDefaults, INetFwMgr::RestoreDefaults, RestoreDefaults, RestoreDefaults method [ICS/ICF], RestoreDefaults method [ICS/ICF],INetFwMgr interface, ics.inetfwmgr_restoredefaults, netfw/INetFwMgr::RestoreDefaults
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetFwMgr::RestoreDefaults
 - netfw/INetFwMgr::RestoreDefaults
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
 - Hnetcfg.dll
api_name:
 - INetFwMgr.RestoreDefaults
---

# INetFwMgr::RestoreDefaults


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Restores the local configuration to its default, installed state.



## -returns

<h3>C++</h3>
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
The operation was stopped because of permissions issues.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
</table>
 

<h3>VB</h3>
If the method succeeds, the return value is S_OK.

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
The operation was stopped because of permissions issues.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
</table>

## -remarks

This method deletes all user and application-added applications and ports that return the system to its installed state. This includes restoring the defaults for Internet Connection Sharing.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwmgr">INetFwMgr</a>



<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwmgr-isicmptypeallowed">INetFwMgr::IsIcmpTypeAllowed</a>



<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwmgr-isportallowed">INetFwMgr::IsPortAllowed</a>

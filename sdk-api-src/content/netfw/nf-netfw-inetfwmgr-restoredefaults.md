---
UID: NF:netfw.INetFwMgr.RestoreDefaults
title: INetFwMgr::RestoreDefaults
author: windows-sdk-content
description: Restores the local configuration to its default, installed state.
old-location: ics\inetfwmgr_restoredefaults.htm
old-project: ICS
ms.assetid: ed2fd6b6-e449-4bed-aeb4-eb4345f67b12
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: INetFwMgr interface [ICS/ICF],RestoreDefaults method, INetFwMgr.RestoreDefaults, INetFwMgr::RestoreDefaults, RestoreDefaults, RestoreDefaults method [ICS/ICF], RestoreDefaults method [ICS/ICF],INetFwMgr interface, ics.inetfwmgr_restoredefaults, netfw/INetFwMgr::RestoreDefaults
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: NETISO_ERROR_TYPE
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
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetFwMgr::RestoreDefaults


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Restores the local configuration to its default, installed state.


## -parameters






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




<a href="https://msdn.microsoft.com/7534ea10-7553-4ec2-af68-0b0393ffc003">INetFwMgr</a>



<a href="https://msdn.microsoft.com/9ff5ef3b-581e-4ce5-9424-dafb08cfe067">INetFwMgr::IsIcmpTypeAllowed</a>



<a href="https://msdn.microsoft.com/39e68271-8046-470a-af90-17bed770716d">INetFwMgr::IsPortAllowed</a>
 

 


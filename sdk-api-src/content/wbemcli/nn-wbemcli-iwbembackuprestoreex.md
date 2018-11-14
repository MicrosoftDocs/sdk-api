---
UID: NN:wbemcli.IWbemBackupRestoreEx
title: IWbemBackupRestoreEx
author: windows-sdk-content
description: The IWbemBackupRestoreEx interface backs up and restores the contents of the repository.
old-location: wmi\iwbembackuprestoreex.htm
tech.root: WmiSdk
ms.assetid: 5349359a-e15f-4799-abad-f4a5fc3e89ea
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IWbemBackupRestoreEx, IWbemBackupRestoreEx interface [Windows Management Instrumentation], IWbemBackupRestoreEx interface [Windows Management Instrumentation],described, wbemcli/IWbemBackupRestoreEx, wmi.iwbembackuprestoreex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemBackupRestoreEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemBackupRestoreEx interface


## -description


The 
<b>IWbemBackupRestoreEx</b> interface backs up and restores the contents of the repository. The affected content of the repository is static data, such as the class definitions that get compiled into the repository when a Managed Object Format (MOF) file is loaded. The dynamic data supplied through providers is not included. This interface adds the <a href="https://msdn.microsoft.com/ce4f2637-cf30-4087-bd49-b26554f434ca">Pause</a> and <a href="https://msdn.microsoft.com/fa31860b-36f5-4182-a58c-b8747af0e628">Resume</a> methods to the functionality of <a href="https://msdn.microsoft.com/27599145-417b-4ca8-8e25-5fffb2e7008c">IWbemBackupRestore</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemBackupRestoreEx</b> interface inherits from <b>IWbemBackupRestore</b>. <b>IWbemBackupRestoreEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemBackupRestoreEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a4932a2-e580-441b-8d3f-9806c673dff9">Backup</a>
</td>
<td align="left" width="63%">
Backs up and restores the contents of the repository to and from a specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce4f2637-cf30-4087-bd49-b26554f434ca">Pause</a>
</td>
<td align="left" width="63%">
Locks out write operations from the WMI repository.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cc85100-5964-4c76-a0e5-305ee7b1638d">Restore</a>
</td>
<td align="left" width="63%">
Backs up and restores the contents of the repository to and from a specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa31860b-36f5-4182-a58c-b8747af0e628">Resume</a>
</td>
<td align="left" width="63%">
Releases the lock on the WMI repository so that operations can continue as normal.

</td>
</tr>
</table> 


## -remarks



The default mode is the same as setting the force mode flag, which breaks all active connections. This results in remote procedure call (RPC) errors from any active COM connections to WMI until new connections are established.

There can be no active connections to the repository during a restore operation. For this reason, the restore operation fails if default parameters are used and there are active connections. A flag can be specified to break all active connections.

The client making the call must have the correct privilege enabled. Backup requires the <b>SE_RESTORE_NAME</b> privilege, and restoration requires <b>SE_RESTORE_NAME</b>. To enable a privilege, a client application must be running under a user account that has that privilege, and the privilege must be enabled using the Windows <a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a> function.

Any local user can make these calls, but remote users must have the <b>WBEM_FULL_WRITE_REP</b> access right to the root namespace.




## -see-also




<a href="https://msdn.microsoft.com/5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1">COM API for
    WMI</a>
 

 


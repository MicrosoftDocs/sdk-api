---
UID: NN:wbemcli.IWbemBackupRestore
title: IWbemBackupRestore
author: windows-driver-content
description: The IWbemBackupRestore interface backs up and restores the contents of the WMI repository.
old-location: wmi\iwbembackuprestore.htm
old-project: WmiSdk
ms.assetid: 27599145-417b-4ca8-8e25-5fffb2e7008c
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWbemBackupRestore, IWbemBackupRestore interface [Windows Management Instrumentation], IWbemBackupRestore interface [Windows Management Instrumentation],described, WbemBackupRestore, _hmm_iwbembackuprestore, wbemcli/IWbemBackupRestore, wmi.iwbembackuprestore
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
req.typenames: WMI_OBJ_TEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wbemsvc.dll
api_name:
-	IWbemBackupRestore
-	WbemBackupRestore
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemBackupRestore interface


## -description


The 
<b>IWbemBackupRestore</b> interface backs up and restores the contents of the WMI repository. The affected content of the repository is static data, such as the class definitions that are compiled into the repository when a MOF file is loaded. The dynamic data supplied through providers is not included.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemBackupRestore</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemBackupRestore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemBackupRestore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9108b682-aded-43e4-a24a-136155d74ebb">Backup</a>
</td>
<td align="left" width="63%">
Backs up the contents of the repository to a specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73a61c69-0a78-4c38-aaec-a72b644f19b4">Restore</a>
</td>
<td align="left" width="63%">
Restores the contents of the repository from a specified file.

</td>
</tr>
</table> 


## -remarks



The default mode is the same as setting the force mode flag, which breaks all active connections. This results in remote procedure call (RPC) errors from any active COM connections to WMI until new connections are established.

There can be no active connections to the repository during a restore operation. For this reason, the restore operation fails if default parameters are used and there are active connections. A flag can be specified to break all active connections.

<div class="alert"><b>Note</b>  The client making the call must have the proper privilege enabled. Backup requires the <b>SE_RESTORE_NAME</b> privilege, while restoration requires <b>SE_RESTORE_NAME</b>. To enable a privilege, a client application must be running under a user account that has that privilege,  and the privilege must be enabled using the Windows <a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a> function.</div>
<div> </div>
For computers running Windows, any local user can make these calls,  but remote users must have the <b>WBEM_FULL_WRITE_REP</b> access right to the root namespace.




## -see-also




<a href="https://msdn.microsoft.com/5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1">COM API for
    WMI</a>
 

 


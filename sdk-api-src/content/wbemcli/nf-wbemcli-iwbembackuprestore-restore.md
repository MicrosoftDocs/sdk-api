---
UID: NF:wbemcli.IWbemBackupRestore.Restore
title: IWbemBackupRestore::Restore
author: windows-sdk-content
description: The IWbemBackupRestore::Restore method deletes the contents of the current repository and restores them with the contents of a previously specified backup.
old-location: wmi\iwbembackuprestore_restore.htm
old-project: WmiSdk
ms.assetid: 73a61c69-0a78-4c38-aaec-a72b644f19b4
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWbemBackupRestore interface [Windows Management Instrumentation],Restore method, IWbemBackupRestore.Restore, IWbemBackupRestore::Restore, Restore, Restore method [Windows Management Instrumentation], Restore method [Windows Management Instrumentation],IWbemBackupRestore interface, WBEM_FLAG_BACKUP_RESTORE_DEFAULT, WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN, _hmm_iwbembackuprestore_restore, wbemcli/IWbemBackupRestore::Restore, wmi.iwbembackuprestore_restore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WMI_OBJ_TEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemBackupRestore.Restore
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemBackupRestore::Restore


## -description


The <b>IWbemBackupRestore::Restore</b> method deletes the contents of the current repository and restores them with the contents of a previously specified backup.

Because Windows Management Instrumentation (WMI) is the server for this interface and must be stopped to complete this operation successfully, the COM connection is broken if this call is successful.


## -parameters




### -param strRestoreFromFile [in]

Constant, null-terminated string of 16-bit Unicode characters that contains the file name of the file to be restored. The specified file should point to a file previously created with 
<a href="https://msdn.microsoft.com/9108b682-aded-43e4-a24a-136155d74ebb">IWbemBackupRestore::Backup</a>.


### -param lFlags [in]

One of the following flags from the <a href="https://msdn.microsoft.com/00072B9F-B4AE-4308-9E8C-F61D982525B3">WBEM_BACKUP_RESTORE_FLAGS</a> enumeration.



#### WBEM_FLAG_BACKUP_RESTORE_DEFAULT

Does not shut down active clients; returns an error if there are any.



#### WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN

Shuts down any active clients.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within the <b>HRESULT</b>.




## -remarks



The default mode is the same as setting the force-mode flag, which breaks all active connections. This results in remote procedure call (RPC) errors from  active COM connections to WMI—until new connections are established.


#### Examples

The following C++ example shows how to call the <b>IWbemBackupRestore::Restore</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// The pInt variable is of type IWbemBackupRestore*
pInt-&gt;Restore(
        L"c:\\\\Windows\\System32\\wbem\\repository\\back.x",
        WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN
      );</pre>
</td>
</tr>
</table></span></div>



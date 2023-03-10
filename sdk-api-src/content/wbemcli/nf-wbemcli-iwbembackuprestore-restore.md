---
UID: NF:wbemcli.IWbemBackupRestore.Restore
title: IWbemBackupRestore::Restore (wbemcli.h)
description: The IWbemBackupRestore::Restore method deletes the contents of the current repository and restores them with the contents of a previously specified backup.
helpviewer_keywords: ["IWbemBackupRestore interface [Windows Management Instrumentation]","Restore method","IWbemBackupRestore.Restore","IWbemBackupRestore::Restore","Restore","Restore method [Windows Management Instrumentation]","Restore method [Windows Management Instrumentation]","IWbemBackupRestore interface","WBEM_FLAG_BACKUP_RESTORE_DEFAULT","WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN","_hmm_iwbembackuprestore_restore","wbemcli/IWbemBackupRestore::Restore","wmi.iwbembackuprestore_restore"]
old-location: wmi\iwbembackuprestore_restore.htm
tech.root: wmi
ms.assetid: 73a61c69-0a78-4c38-aaec-a72b644f19b4
ms.date: 12/05/2018
ms.keywords: IWbemBackupRestore interface [Windows Management Instrumentation],Restore method, IWbemBackupRestore.Restore, IWbemBackupRestore::Restore, Restore, Restore method [Windows Management Instrumentation], Restore method [Windows Management Instrumentation],IWbemBackupRestore interface, WBEM_FLAG_BACKUP_RESTORE_DEFAULT, WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN, _hmm_iwbembackuprestore_restore, wbemcli/IWbemBackupRestore::Restore, wmi.iwbembackuprestore_restore
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemBackupRestore::Restore
 - wbemcli/IWbemBackupRestore::Restore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemsvc.dll
api_name:
 - IWbemBackupRestore.Restore
---

# IWbemBackupRestore::Restore


## -description

The <b>IWbemBackupRestore::Restore</b> method deletes the contents of the current repository and restores them with the contents of a previously specified backup.

Because Windows Management Instrumentation (WMI) is the server for this interface and must be stopped to complete this operation successfully, the COM connection is broken if this call is successful.

## -parameters

### -param strRestoreFromFile [in]

Constant, null-terminated string of 16-bit Unicode characters that contains the file name of the file to be restored. The specified file should point to a file previously created with 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbembackuprestore-backup">IWbemBackupRestore::Backup</a>.

### -param lFlags [in]

One of the following flags from the <a href="/windows/win32/api/wbemcli/ne-wbemcli-wbem_backup_restore_flags">WBEM_BACKUP_RESTORE_FLAGS</a> enumeration.



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


```cpp
// The pInt variable is of type IWbemBackupRestore*
pInt->Restore(
        L"c:\\\\Windows\\System32\\wbem\\repository\\back.x",
        WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN
      );
```
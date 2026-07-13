---
UID: NF:wsbonline.DeregisterOnlineBackupFromWindowsServerBackup
title: DeregisterOnlineBackupFromWindowsServerBackup function (wsbonline.h)
description: De-registers an already registered Cloud backup provider.
helpviewer_keywords: ["DeregisterOnlineBackupFromWindowsServerBackup","DeregisterOnlineBackupFromWindowsServerBackup function [Windows Server Backup]","wsb.deregisteronlinebackupfromwindowsserverbackup","wsbonline/DeregisterOnlineBackupFromWindowsServerBackup"]
old-location: wsb\deregisteronlinebackupfromwindowsserverbackup.htm
tech.root: wsb
ms.assetid: 4E70EF3D-E4AA-498C-B131-8C5F48CD230E
ms.date: 12/05/2018
ms.keywords: DeregisterOnlineBackupFromWindowsServerBackup, DeregisterOnlineBackupFromWindowsServerBackup function [Windows Server Backup], wsb.deregisteronlinebackupfromwindowsserverbackup, wsbonline/DeregisterOnlineBackupFromWindowsServerBackup
req.header: wsbonline.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: wsbonline.lib
req.dll: WsbOnline.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DeregisterOnlineBackupFromWindowsServerBackup
 - wsbonline/DeregisterOnlineBackupFromWindowsServerBackup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsbOnline.dll
api_name:
 - DeregisterOnlineBackupFromWindowsServerBackup
---

# DeregisterOnlineBackupFromWindowsServerBackup function


## -description

The 
  <b>DeregisterOnlineBackupFromWindowsServerBackup</b> 
  function de-registers an already registered cloud backup provider.

## -parameters

### -param guidSnapinId [in]

The snap-in identifier of the cloud backup provider to be de-registered with Windows Server Backup.

## -returns

The return values listed here are in addition to the normal <b>HRESULT</b>s that may 
    be returned at any time from the function.

## -see-also

<a href="/previous-versions/windows/desktop/wsb/windows-server-backup-api-functions">Cloud  Backup Provider API Functions</a>
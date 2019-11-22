---
UID: NF:wsbonline.RegisterOnlineBackupWithWindowsServerBackup
title: RegisterOnlineBackupWithWindowsServerBackup function (wsbonline.h)

description: Registers a Cloud backup provider with Windows Server Backup.
old-location: wsb\registeronlinebackupwithwindowsserverbackup.htm
tech.root: wsb
ms.assetid: F6BBE44C-E735-47E9-8AD1-A7F1FBAC0330

ms.date: 12/05/2018
ms.keywords: RegisterOnlineBackupWithWindowsServerBackup, RegisterOnlineBackupWithWindowsServerBackup function [Windows Server Backup], wsb.registeronlinebackupwithwindowsserverbackup, wsbonline/RegisterOnlineBackupWithWindowsServerBackup
ms.topic: function
f1_keywords:
- wsbonline/RegisterOnlineBackupWithWindowsServerBackup
dev_langs:
 - c++
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
req.lib: 
req.dll: WsbOnline.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- WsbOnline.dll
api_name:
- RegisterOnlineBackupWithWindowsServerBackup
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RegisterOnlineBackupWithWindowsServerBackup function


## -description


The <b>RegisterOnlineBackupWithWindowsServerBackup</b> function registers a cloud backup provider with Windows Server Backup.


## -parameters




### -param pOBRegistrationInfo [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wsbonline/ns-wsbonline-wsb_ob_registration_info">WSB_OB_REGISTRATION_INFO</a> structure.


## -returns



The return values listed here are in addition to the normal <b>HRESULT</b>s that may be returned at any time 
       from the function.




## -remarks



If any other cloud backup provider is already registered with Windows Server Backup, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wsbonline/nf-wsbonline-deregisteronlinebackupfromwindowsserverbackup">DeregisterOnlineBackupFromWindowsServerBackup</a> must be called before calling <b>RegisterOnlineBackupWithWindowsServerBackup</b>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wsb/windows-server-backup-api-functions">Cloud  Backup Provider API Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wsbonline/ns-wsbonline-wsb_ob_registration_info">WSB_OB_REGISTRATION_INFO</a>
 

 


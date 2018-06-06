---
UID: NF:wsbonline.DeregisterOnlineBackupFromWindowsServerBackup
title: DeregisterOnlineBackupFromWindowsServerBackup function
author: windows-sdk-content
description: De-registers an already registered Cloud backup provider.
old-location: wsb\deregisteronlinebackupfromwindowsserverbackup.htm
old-project: wsb
ms.assetid: 4E70EF3D-E4AA-498C-B131-8C5F48CD230E
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: DeregisterOnlineBackupFromWindowsServerBackup, DeregisterOnlineBackupFromWindowsServerBackup function [Windows Server Backup], wsb.deregisteronlinebackupfromwindowsserverbackup, wsbonline/DeregisterOnlineBackupFromWindowsServerBackup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WSB_OB_STATUS_ENTRY_PAIR_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsbOnline.dll
api_name:
 - DeregisterOnlineBackupFromWindowsServerBackup
product: Windows
targetos: Windows
req.lib: 
req.dll: WsbOnline.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/61F77E92-19EF-4409-9435-CD03ACCE810D">Cloud  Backup Provider API Functions</a>
 

 


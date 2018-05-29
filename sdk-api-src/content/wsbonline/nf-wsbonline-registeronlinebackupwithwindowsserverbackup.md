---
UID: NF:wsbonline.RegisterOnlineBackupWithWindowsServerBackup
title: RegisterOnlineBackupWithWindowsServerBackup function
author: windows-sdk-content
description: Registers a Cloud backup provider with Windows Server Backup.
old-location: wsb\registeronlinebackupwithwindowsserverbackup.htm
old-project: wsb
ms.assetid: F6BBE44C-E735-47E9-8AD1-A7F1FBAC0330
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: RegisterOnlineBackupWithWindowsServerBackup, RegisterOnlineBackupWithWindowsServerBackup function [Windows Server Backup], wsb.registeronlinebackupwithwindowsserverbackup, wsbonline/RegisterOnlineBackupWithWindowsServerBackup
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
req.typenames: WSB_OB_STATUS_ENTRY_PAIR_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WsbOnline.dll
api_name:
-	RegisterOnlineBackupWithWindowsServerBackup
product: Windows
targetos: Windows
req.lib: 
req.dll: WsbOnline.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegisterOnlineBackupWithWindowsServerBackup function


## -description


The <b>RegisterOnlineBackupWithWindowsServerBackup</b> function registers a cloud backup provider with Windows Server Backup.


## -parameters




### -param pOBRegistrationInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/E01EF90E-90F1-4B56-85B8-63A10A688FBA">WSB_OB_REGISTRATION_INFO</a> structure.


## -returns



The return values listed here are in addition to the normal <b>HRESULT</b>s that may be returned at any time 
       from the function.




## -remarks



If any other cloud backup provider is already registered with Windows Server Backup, <a href="https://msdn.microsoft.com/4E70EF3D-E4AA-498C-B131-8C5F48CD230E">DeregisterOnlineBackupFromWindowsServerBackup</a> must be called before calling <b>RegisterOnlineBackupWithWindowsServerBackup</b>.




## -see-also




<a href="https://msdn.microsoft.com/61F77E92-19EF-4409-9435-CD03ACCE810D">Cloud  Backup Provider API Functions</a>



<a href="https://msdn.microsoft.com/E01EF90E-90F1-4B56-85B8-63A10A688FBA">WSB_OB_REGISTRATION_INFO</a>
 

 


---
UID: NF:wbemcli.IWbemBackupRestore.Backup
title: IWbemBackupRestore::Backup
author: windows-sdk-content
description: The IWbemBackupRestore::Backup method backs up the contents of the static repository to a separate file.
old-location: wmi\iwbembackuprestore_backup.htm
old-project: WmiSdk
ms.assetid: 9108b682-aded-43e4-a24a-136155d74ebb
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: Backup, Backup method [Windows Management Instrumentation], Backup method [Windows Management Instrumentation],IWbemBackupRestore interface, IWbemBackupRestore interface [Windows Management Instrumentation],Backup method, IWbemBackupRestore.Backup, IWbemBackupRestore::Backup, _hmm_iwbembackuprestore_backup, wbemcli/IWbemBackupRestore::Backup, wmi.iwbembackuprestore_backup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.redist: 
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
 - IWbemBackupRestore.Backup
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wbemsvc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemBackupRestore::Backup


## -description


The <b>IWbemBackupRestore::Backup</b> method backs up the contents of the static repository to a separate file.


## -parameters




### -param strBackupToFile [in]

Constant, null-terminated string of 16-bit Unicode characters that contains the file name to which to back up the contents of the repository.


### -param lFlags [in]

Reserved. This parameter must be 0 (zero).


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.




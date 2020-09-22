---
UID: NF:gpmgmt.IGPMBackupDir.GetBackup
title: IGPMBackupDir::GetBackup (gpmgmt.h)
description: Retrieves the GPMBackup object that has the specified backup ID (GUID). The backup ID is the ID of the backed-up GPO, not the ID of the GPO.
helpviewer_keywords: ["GPMBackupDir object [GPMC]","GetBackup method","GetBackup","GetBackup method [GPMC]","GetBackup method [GPMC]","GPMBackupDir object","GetBackup method [GPMC]","IGPMBackupDir interface","IGPMBackupDir interface [GPMC]","GetBackup method","IGPMBackupDir.GetBackup","IGPMBackupDir::GetBackup","_win32_igpmbackupdir_getbackup","gpmc.igpmbackupdir_getbackup","gpmgmt/IGPMBackupDir::GetBackup"]
old-location: gpmc\igpmbackupdir_getbackup.htm
tech.root: gpmc
ms.assetid: 45f286dc-fa60-4cfd-bdf0-bfeaf2a5a396
ms.date: 12/05/2018
ms.keywords: GPMBackupDir object [GPMC],GetBackup method, GetBackup, GetBackup method [GPMC], GetBackup method [GPMC],GPMBackupDir object, GetBackup method [GPMC],IGPMBackupDir interface, IGPMBackupDir interface [GPMC],GetBackup method, IGPMBackupDir.GetBackup, IGPMBackupDir::GetBackup, _win32_igpmbackupdir_getbackup, gpmc.igpmbackupdir_getbackup, gpmgmt/IGPMBackupDir::GetBackup
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMBackupDir::GetBackup
 - gpmgmt/IGPMBackupDir::GetBackup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMBackupDir.GetBackup
 - GPMBackupDir.GetBackup
---

## -description

Retrieves the <b>GPMBackup</b> object that has the specified backup ID (GUID). The backup ID is the ID of the backed-up GPO, not the ID of the GPO.

## -parameters

### -param bstrID [in]

ID of the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a> object to open.

### -param ppBackup [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a> interface for the specified ID.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">IGPMBackupCollection</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdir">IGPMBackupDir</a>
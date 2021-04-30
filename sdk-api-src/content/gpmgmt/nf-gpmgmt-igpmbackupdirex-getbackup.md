---
UID: NF:gpmgmt.IGPMBackupDirEx.GetBackup
title: IGPMBackupDirEx::GetBackup (gpmgmt.h)
description: Retrieves the GPMBackup or GPMStarterGPOBackup object with the specified backup ID. The backup ID is a GUID. The backup ID is the ID of the backed-up Group Policy object (GPO), not the ID of the GPO.
helpviewer_keywords: ["GetBackup","GetBackup method [GPMC]","GetBackup method [GPMC]","IGPMBackupDirEx interface","IGPMBackupDirEx interface [GPMC]","GetBackup method","IGPMBackupDirEx.GetBackup","IGPMBackupDirEx::GetBackup","gpmc.igpmbackupdirex_getbackup","gpmgmt/IGPMBackupDirEx::GetBackup"]
old-location: gpmc\igpmbackupdirex_getbackup.htm
tech.root: gpmc
ms.assetid: d1c6ead9-882d-4041-9586-f08a83f4c9b0
ms.date: 12/05/2018
ms.keywords: GetBackup, GetBackup method [GPMC], GetBackup method [GPMC],IGPMBackupDirEx interface, IGPMBackupDirEx interface [GPMC],GetBackup method, IGPMBackupDirEx.GetBackup, IGPMBackupDirEx::GetBackup, gpmc.igpmbackupdirex_getbackup, gpmgmt/IGPMBackupDirEx::GetBackup
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
 - IGPMBackupDirEx::GetBackup
 - gpmgmt/IGPMBackupDirEx::GetBackup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gpmgmt.dll
api_name:
 - IGPMBackupDirEx.GetBackup
---

# IGPMBackupDirEx::GetBackup


## -description

Retrieves the <b>GPMBackup</b> or <b>GPMStarterGPOBackup</b> object with the specified backup ID. The backup ID is a GUID. The backup ID is the ID of the backed-up Group Policy object (GPO), not the ID of the GPO.

## -parameters

### -param bstrID [in]

ID of the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> or <b>GPMStarterGPOBackup</b> object to open.

### -param pvarBackup [out]

Pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a> or <b>IGPMStarterGPOBackup</b> interface for the ID specified.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> or <b>GPMStarterGPOBackup</b> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> or <b>GPMStarterGPOBackup</b> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">IGPMBackupCollection</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdirex">IGPMBackupDirEx</a>



<b>IGPMStarterGPOBackup</b>



<b>IGPMStarterGPOBackupCollection</b>
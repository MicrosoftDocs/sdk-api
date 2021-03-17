---
UID: NF:gpmgmt.IGPM.GetBackupDir
title: IGPM::GetBackupDir (gpmgmt.h)
description: Creates and returns a GPMBackupDir object, which you can use to access the GPMBackup and GPMBackupCollection objects.
helpviewer_keywords: ["GPM class [GPMC]","GetBackupDir method","GetBackupDir","GetBackupDir method [GPMC]","GetBackupDir method [GPMC]","GPM class","GetBackupDir method [GPMC]","IGPM interface","IGPM interface [GPMC]","GetBackupDir method","IGPM.GetBackupDir","IGPM::GetBackupDir","_win32_igpm_getbackupdir","gpmc.igpm_getbackupdir","gpmgmt/IGPM::GetBackupDir"]
old-location: gpmc\igpm_getbackupdir.htm
tech.root: gpmc
ms.assetid: 4ffc8827-8427-4ee5-ad89-21f821d16d97
ms.date: 12/05/2018
ms.keywords: GPM class [GPMC],GetBackupDir method, GetBackupDir, GetBackupDir method [GPMC], GetBackupDir method [GPMC],GPM class, GetBackupDir method [GPMC],IGPM interface, IGPM interface [GPMC],GetBackupDir method, IGPM.GetBackupDir, IGPM::GetBackupDir, _win32_igpm_getbackupdir, gpmc.igpm_getbackupdir, gpmgmt/IGPM::GetBackupDir
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
 - IGPM::GetBackupDir
 - gpmgmt/IGPM::GetBackupDir
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
 - IGPM.GetBackupDir
 - GPM.GetBackupDir
---

# IGPM::GetBackupDir


## -description

Creates and returns a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdir">GPMBackupDir</a> object, which you can use to access 
the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> and 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">GPMBackupCollection</a> objects.

## -parameters

### -param bstrBackupDir [in]

Required.  The name of the file system directory that contains the Group Policy object (GPO) backups. The directory must already exist.

### -param pIGPMBackupDir [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdir">IGPMBackupDir</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs

<h3>JScript</h3>
Returns a reference to a <b>GPMBackupDir</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMBackupDir</b> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">IGPMBackupCollection</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdir">IGPMBackupDir</a>
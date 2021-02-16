---
UID: NF:gpmgmt.IGPM2.GetBackupDirEx
title: IGPM2::GetBackupDirEx (gpmgmt.h)
description: For a Group Policy object (GPO), the GetBackupDirEx method creates and returns a GPMBackupDirEx object, which you can use to access a GPMBackup or GPMBackupCollection object.
helpviewer_keywords: ["GetBackupDirEx","GetBackupDirEx method [GPMC]","GetBackupDirEx method [GPMC]","IGPM2 interface","IGPM2 interface [GPMC]","GetBackupDirEx method","IGPM2.GetBackupDirEx","IGPM2::GetBackupDirEx","gpmc.igpm2_getbackupdirex","gpmgmt/IGPM2::GetBackupDirEx"]
old-location: gpmc\igpm2_getbackupdirex.htm
tech.root: gpmc
ms.assetid: 2fe4ea93-6668-4534-b72e-71b1062db627
ms.date: 12/05/2018
ms.keywords: GetBackupDirEx, GetBackupDirEx method [GPMC], GetBackupDirEx method [GPMC],IGPM2 interface, IGPM2 interface [GPMC],GetBackupDirEx method, IGPM2.GetBackupDirEx, IGPM2::GetBackupDirEx, gpmc.igpm2_getbackupdirex, gpmgmt/IGPM2::GetBackupDirEx
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
 - IGPM2::GetBackupDirEx
 - gpmgmt/IGPM2::GetBackupDirEx
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
 - IGPM2.GetBackupDirEx
---

# IGPM2::GetBackupDirEx


## -description

For a Group Policy object (GPO), the <b>GetBackupDirEx</b> method creates and returns a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdir">GPMBackupDirEx</a> object, which you can use to access 
a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> or <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">GPMBackupCollection</a> object.

For a Starter Group Policy object, the <b>GetBackupDirEx</b> method creates and returns a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdir">GPMBackupDirEx</a> object, which you can use to access 
a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackup">GPMStarterGPOBackup</a> or <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackupcollection">GPMStarterGPOBackupCollection</a> object.

## -parameters

### -param bstrBackupDir [in]

Required. The name of the file system directory containing the Group Policy object (GPO) backups. Note that the directory must already exist.

### -param backupDirType [in]

Determines whether the back up is for a Starter Group Policy object or a Group Policy object.

### -param ppIGPMBackupDirEx [out, retval]

Address of a pointer to the   <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdirex">IGPMBackupDirEx</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdirex">GPMBackupDirEx</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdirex">GPMBackupDirEx</a> object.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm2">IGPM2</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">IGPMBackupCollection</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdir">IGPMBackupDir</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackup">IGPMStarterGPOBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpobackupcollection">IGPMStarterGPOBackupCollection</a>
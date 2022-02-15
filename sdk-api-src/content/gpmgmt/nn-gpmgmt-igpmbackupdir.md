---
UID: NN:gpmgmt.IGPMBackupDir
title: IGPMBackupDir (gpmgmt.h)
description: The IGPMBackupDir interface supports methods that allow you to query GPMBackup and GPMBackupCollection objects when you use the Group Policy Management Console (GPMC) interfaces.
helpviewer_keywords: ["GPMBackupDir","IGPMBackupDir","IGPMBackupDir interface [GPMC]","IGPMBackupDir interface [GPMC]","described","_win32_igpmbackupdir","gpmc.igpmbackupdir","gpmgmt/IGPMBackupDir"]
old-location: gpmc\igpmbackupdir.htm
tech.root: gpmc
ms.assetid: 2d44cf6d-a3fa-43db-b28e-3d48f6d13625
ms.date: 12/05/2018
ms.keywords: GPMBackupDir, IGPMBackupDir, IGPMBackupDir interface [GPMC], IGPMBackupDir interface [GPMC],described, _win32_igpmbackupdir, gpmc.igpmbackupdir, gpmgmt/IGPMBackupDir
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
 - IGPMBackupDir
 - gpmgmt/IGPMBackupDir
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
 - IGPMBackupDir
 - GPMBackupDir
---

# IGPMBackupDir interface


## -description

The 
<b>IGPMBackupDir</b> interface supports methods that allow you to query 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> and 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">GPMBackupCollection</a> objects when you use the Group Policy Management Console (GPMC) interfaces.

To create a <b>GPMBackupDir</b> object, call the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-getbackupdir">IGPM::GetBackupDir</a> method.

## -inheritance

The <b>IGPMBackupDir</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMBackupDir</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">IGPMBackupCollection</a>

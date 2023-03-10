---
UID: NF:gpmgmt.IGPMBackupDirEx.SearchBackups
title: IGPMBackupDirEx::SearchBackups (gpmgmt.h)
description: Executes a search for a GPMBackup object or an IGPMStarterGPOBackup interface according to the specified criteria, and returns a GPMBackupCollection or GPMStarterGPOBackupCollection object.
helpviewer_keywords: ["GPMBackupDirEx object [GPMC]","SearchBackups method","IGPMBackupDirEx interface [GPMC]","SearchBackups method","IGPMBackupDirEx.SearchBackups","IGPMBackupDirEx::SearchBackups","SearchBackups","SearchBackups method [GPMC]","SearchBackups method [GPMC]","GPMBackupDirEx object","SearchBackups method [GPMC]","IGPMBackupDirEx interface","backupMostRecent","gpmc.igpmbackupdirex_searchbackups","gpmgmt/IGPMBackupDirEx::SearchBackups","gpoDisplayName","gpoDomain","gpoID"]
old-location: gpmc\igpmbackupdirex_searchbackups.htm
tech.root: gpmc
ms.assetid: e45f012e-ce88-4baf-88a2-bd61e365b291
ms.date: 12/05/2018
ms.keywords: GPMBackupDirEx object [GPMC],SearchBackups method, IGPMBackupDirEx interface [GPMC],SearchBackups method, IGPMBackupDirEx.SearchBackups, IGPMBackupDirEx::SearchBackups, SearchBackups, SearchBackups method [GPMC], SearchBackups method [GPMC],GPMBackupDirEx object, SearchBackups method [GPMC],IGPMBackupDirEx interface, backupMostRecent, gpmc.igpmbackupdirex_searchbackups, gpmgmt/IGPMBackupDirEx::SearchBackups, gpoDisplayName, gpoDomain, gpoID
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
 - IGPMBackupDirEx::SearchBackups
 - gpmgmt/IGPMBackupDirEx::SearchBackups
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
 - IGPMBackupDirEx.SearchBackups
 - GPMBackupDirEx.SearchBackups
---

## -description

Executes a search for  a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> object or an <b>IGPMStarterGPOBackup</b> interface according to the specified criteria, and returns a 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">GPMBackupCollection</a> or <b>GPMStarterGPOBackupCollection</b> object.

## -parameters

### -param pIGPMSearchCriteria [in]

Pointer to the criteria to be applied to the search.

### -param pvarBackupCollection [out]

Pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">IGPMBackupCollection</a> or <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">IGPMStarterGPOBackupCollection</a> interface that represent the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a> or <b>IGPMStarterGPOBackup</b> objects that are found by the search.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMBackupCollection</b> or <b>GPMStarterGPOBackupCollection</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMBackupCollection</b> or <b>GPMStarterGPOBackupCollection</b> object.

## -remarks

An empty  <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">IGPMSearchCriteria</a> interface or <b>GPMSearchCriteria</b> object has had no criteria added to it. Passing in an empty <b>IGPMSearchCriteria</b> interface or <b>GPMSearchCriteria</b> object will return all  
information in the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a> or <b>IGPMStarterGPOBackup</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">IGPMBackupCollection</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdirex">IGPMBackupDirEx</a>



<b>IGPMStarterGPOBackup</b>



<b>IGPMStarterGPOBackupCollection</b>
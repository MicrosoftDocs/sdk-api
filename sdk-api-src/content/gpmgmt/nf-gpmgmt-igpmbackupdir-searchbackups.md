---
UID: NF:gpmgmt.IGPMBackupDir.SearchBackups
title: IGPMBackupDir::SearchBackups (gpmgmt.h)
description: Executes a search for the GPMBackup object according to the specified criteria, and returns a GPMBackupCollection object.
helpviewer_keywords: ["GPMBackupDir object [GPMC]","SearchBackups method","IGPMBackupDir interface [GPMC]","SearchBackups method","IGPMBackupDir.SearchBackups","IGPMBackupDir::SearchBackups","SearchBackups","SearchBackups method [GPMC]","SearchBackups method [GPMC]","GPMBackupDir object","SearchBackups method [GPMC]","IGPMBackupDir interface","_win32_igpmbackupdir_searchbackups","backupMostRecent","gpmc.igpmbackupdir_searchbackups","gpmgmt/IGPMBackupDir::SearchBackups","gpoDisplayName","gpoDomain","gpoID"]
old-location: gpmc\igpmbackupdir_searchbackups.htm
tech.root: gpmc
ms.assetid: 71e1991f-c24f-43fe-8f3e-83f5b02cec6b
ms.date: 12/05/2018
ms.keywords: GPMBackupDir object [GPMC],SearchBackups method, IGPMBackupDir interface [GPMC],SearchBackups method, IGPMBackupDir.SearchBackups, IGPMBackupDir::SearchBackups, SearchBackups, SearchBackups method [GPMC], SearchBackups method [GPMC],GPMBackupDir object, SearchBackups method [GPMC],IGPMBackupDir interface, _win32_igpmbackupdir_searchbackups, backupMostRecent, gpmc.igpmbackupdir_searchbackups, gpmgmt/IGPMBackupDir::SearchBackups, gpoDisplayName, gpoDomain, gpoID
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
 - IGPMBackupDir::SearchBackups
 - gpmgmt/IGPMBackupDir::SearchBackups
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
 - IGPMBackupDir.SearchBackups
 - GPMBackupDir.SearchBackups
---

# IGPMBackupDir::SearchBackups


## -description

Executes a search for 
the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> object according to the specified criteria, and returns an  
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">GPMBackupCollection</a> object.

## -parameters

### -param pIGPMSearchCriteria [in]

Pointer to the criteria to apply to the search.



#### gpoDomain

Pointer to   the criteria for a search for a domain name.  The search property value is the domain name.  The <b>opEquals</b> or <b>opNotEquals</b> operators are valid search criteria.



#### gpoID

Pointer to criteria for a search for a Group Policy object (GPO) ID. The search property value is the GPO ID.  The <b>opEquals</b> or <b>opNotEquals</b> operators are valid search criteria.



#### gpoDisplayName

Pointer to criteria for a search for   a GPO display name. The search property value is the GPO display name. The <b>opEquals</b>, <b>opContains</b>, or <b>opNotContains</b> operators are valid search criteria.



#### backupMostRecent

Pointer to criteria for a search for the most recent backup. The search property value is <b>TRUE</b>. The   <b>opEquals</b>  operator is the valid search criteria.

### -param ppIGPMBackupCollection [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">IGPMBackupCollection</a> interface that represents the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a> objects found by the search.


#### - objGPMSearchCriteria [in]


<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">GPMSearchCriteria</a> object to apply to the search.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMBackupCollection</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMBackupCollection</b> object.

## -remarks

An empty  <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsearchcriteria">GPMSearchCriteria</a> has had no criteria added to it. Passing in an empty <b>GPMSearchCriteria</b> will return all  
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> objects.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">IGPMBackupCollection</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdir">IGPMBackupDir</a>
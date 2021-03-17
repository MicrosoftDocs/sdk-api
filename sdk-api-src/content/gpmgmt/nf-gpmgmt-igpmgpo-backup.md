---
UID: NF:gpmgmt.IGPMGPO.Backup
title: IGPMGPO::Backup (gpmgmt.h)
description: Backs up a Group Policy object (GPO) to the specified directory.
helpviewer_keywords: ["Backup","Backup method [GPMC]","Backup method [GPMC]","GPMGPO object","Backup method [GPMC]","IGPMGPO interface","GPMGPO object [GPMC]","Backup method","IGPMGPO interface [GPMC]","Backup method","IGPMGPO.Backup","IGPMGPO::Backup","_win32_igpmgpo_backup","gpmc.igpmgpo_backup","gpmgmt/IGPMGPO::Backup"]
old-location: gpmc\igpmgpo_backup.htm
tech.root: gpmc
ms.assetid: 5ba8d2f7-4989-4882-9ceb-4f77b8745442
ms.date: 12/05/2018
ms.keywords: Backup, Backup method [GPMC], Backup method [GPMC],GPMGPO object, Backup method [GPMC],IGPMGPO interface, GPMGPO object [GPMC],Backup method, IGPMGPO interface [GPMC],Backup method, IGPMGPO.Backup, IGPMGPO::Backup, _win32_igpmgpo_backup, gpmc.igpmgpo_backup, gpmgmt/IGPMGPO::Backup
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
 - IGPMGPO::Backup
 - gpmgmt/IGPMGPO::Backup
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
 - IGPMGPO.Backup
 - GPMGPO.Backup
---

# IGPMGPO::Backup


## -description

Backs up a Group Policy object (GPO) to the specified directory. A backup operation transfers the contents of a GPO from the Active Directory directory service to the file system. The backup includes the policy settings, the GPO ID, and any 
<a href="/windows/desktop/SecAuthZ/access-control-lists">access control lists</a> (ACLs) that are associated with the GPO. This method is also used for exporting GPOs to the file system.

## -parameters

### -param bstrBackupDir [in]

Name of the file system directory in which the  <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> object should be stored. The directory must already exist.

### -param bstrComment [in]

Comment to associate with the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> object.

### -param pvarGPMProgress [in, optional]

Specifies a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of the backup operation. The method runs synchronously if this parameter is <b>NULL</b>. The method runs asynchronously if this parameter is not <b>NULL</b>. This parameter must be <b>NULL</b> if the client should not receive asynchronous notifications.

### -param pvarGPMCancel [out, optional]

Receives a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a> interface that the client can use to cancel the backup operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.

### -param ppIGPMResult [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a> interface that represents the result of the backup operation. That interface contains pointers to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a> interface and to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

## -remarks

A GPO that has been backed-up (also called exported) can be restored to the Active Directory by calling the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-restoregpo">IGPMDomain::RestoreGPO</a> method or imported into another existing GPO using the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-import">IGPMGPO::Import</a> method, depending on the required result.

You must check the code that is returned by the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmresult-overallstatus">IGPMResult::OverallStatus</a> method as well as the one that is returned by this method to determine whether the operation succeeded. 
<b>OverallStatus</b> returns an overall status code for the operation. If no error occurred during the operation, it returns a success code. Otherwise, it returns a failure code.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a>
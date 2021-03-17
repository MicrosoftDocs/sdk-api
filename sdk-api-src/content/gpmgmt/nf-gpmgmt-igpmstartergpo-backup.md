---
UID: NF:gpmgmt.IGPMStarterGPO.Backup
title: IGPMStarterGPO::Backup (gpmgmt.h)
description: Creates a backup of the current Starter GPO.
helpviewer_keywords: ["Backup","Backup method [GPMC]","Backup method [GPMC]","IGPMStarterGPO interface","IGPMStarterGPO interface [GPMC]","Backup method","IGPMStarterGPO.Backup","IGPMStarterGPO::Backup","gpmc.igpmstartergpo_backup","gpmgmt/IGPMStarterGPO::Backup"]
old-location: gpmc\igpmstartergpo_backup.htm
tech.root: gpmc
ms.assetid: bf419f56-803f-44c2-ae08-7e428940f79d
ms.date: 12/05/2018
ms.keywords: Backup, Backup method [GPMC], Backup method [GPMC],IGPMStarterGPO interface, IGPMStarterGPO interface [GPMC],Backup method, IGPMStarterGPO.Backup, IGPMStarterGPO::Backup, gpmc.igpmstartergpo_backup, gpmgmt/IGPMStarterGPO::Backup
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
 - IGPMStarterGPO::Backup
 - gpmgmt/IGPMStarterGPO::Backup
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
 - IGPMStarterGPO.Backup
---

# IGPMStarterGPO::Backup


## -description

Creates a backup of the current Starter GPO.

## -parameters

### -param bstrBackupDir [in]

Name of the file system directory in which the <b>GPMStarterGPOBackup</b> object should be stored.  The directory must already exist.  Use a null-terminated string.

### -param bstrComment [in]

Comment to associate with the <b>GPMStarterGPOBackup</b> object.

### -param pvarGPMProgress [in, optional]

Specifies a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of the backup operation. The method runs synchronously if this parameter is <b>NULL</b>. The method runs asynchronously if this parameter is not <b>NULL</b>. This parameter must be <b>NULL</b> if the client should not receive asynchronous notifications.

### -param pvarGPMCancel [out, optional]

Receives a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a> interface that the client can use to cancel the backup operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.

### -param ppIGPMResult [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a> interface representing the result of the backup operation. That interface contains pointers to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a> interface and an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a> interface.

## -returns

Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

For more information, see the following Remarks section.

## -remarks

Note that you must check the code returned by the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmresult-overallstatus">IGPMResult::OverallStatus</a> method as well as the one returned by this method to determine whether or not the operation succeeded. 
<b>OverallStatus</b> returns an overall status code for the operation. If no error occurred during the operation, it returns a success code; otherwise it returns a failure code.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstartergpo">IGPMStarterGPO</a>
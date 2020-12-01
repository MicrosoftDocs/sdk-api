---
UID: NF:gpmgmt.IGPMGPO.Import
title: IGPMGPO::Import (gpmgmt.h)
description: Imports the policy settings from the specified GPMBackup object.
helpviewer_keywords: ["GPMGPO object [GPMC]","Import method","IGPMGPO interface [GPMC]","Import method","IGPMGPO.Import","IGPMGPO::Import","Import","Import method [GPMC]","Import method [GPMC]","GPMGPO object","Import method [GPMC]","IGPMGPO interface","_win32_igpmgpo_import","gpmc.igpmgpo_import","gpmgmt/IGPMGPO::Import"]
old-location: gpmc\igpmgpo_import.htm
tech.root: gpmc
ms.assetid: 3b16eefb-89af-408b-a84c-c8ab958b4cc7
ms.date: 12/05/2018
ms.keywords: GPMGPO object [GPMC],Import method, IGPMGPO interface [GPMC],Import method, IGPMGPO.Import, IGPMGPO::Import, Import, Import method [GPMC], Import method [GPMC],GPMGPO object, Import method [GPMC],IGPMGPO interface, _win32_igpmgpo_import, gpmc.igpmgpo_import, gpmgmt/IGPMGPO::Import
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
 - IGPMGPO::Import
 - gpmgmt/IGPMGPO::Import
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
 - IGPMGPO.Import
 - GPMGPO.Import
---

## -description

Imports the policy settings from the specified 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> object. An import operation transfers the policy settings from a backed-up GPO in the file system to a GPO in the Active Directory. The operation erases any previous policy settings in the destination GPO. The source GPO can be any backed-up GPO in the file system and the destination GPO must be an existing GPO in the Active Directory.

## -parameters

### -param lFlags [in]

Specifies the options to use for security principal and path mapping. The following options are defined. For more information, see 
<a href="/previous-versions/windows/desktop/gpmc/copying-and-importing-gpos-across-domains">Copying and Importing GPOs Across Domains</a>.

#### 0

Map the Security principal and UNC path from the migration table if specified. If there is no entry corresponding to Security principal or UNCPath, keep the setting containing that Security principal or UNC Path as it is. Do not copy security on the GPO and Software Installation Package objects. This is the default value for this parameter.

#### GPM_MIGRATIONTABLE_ONLY

Map the security principals and UNC paths using the information specified in the migration table only. If a setting is found that cannot be mapped through the migration table, the method fails and returns an error code.

### -param pIGPMBackup [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> object from which settings should be imported.

### -param pvarMigrationTable [in, optional]

Pointer to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmmigrationtable">IGPMMigrationTable</a> to use for mapping.  This parameter can be <b>NULL</b>.

### -param pvarGPMProgress [in, optional]

Specifies a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress</a> interface that allows the client to receive status notifications about the progress of the import operation. This parameter must be <b>NULL</b> if the client should not receive asynchronous notifications.

### -param pvarGPMCancel [out, optional]

Receives a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a> interface that the client can use to cancel the import operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.

### -param ppIGPMResult [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a> interface representing the result of the import operation. That interface contains a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a> interface and an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

## -remarks

An import operation only transfers policy settings. It erases any existing settings in the GPO. An import does not modify the GPO ID or the <a href="/windows/desktop/SecAuthZ/access-control-lists">ACLs</a> on the destination GPO, nor does it modify any links that point to the destination GPO or to an associated WMI filter.

<div class="alert"><b>Note</b>  An import operation is similar but different than a copy operation. For an import operation, the source GPO must be in the file system and the destination must be an existing GPO in Active Directory. For a copy operation, the source GPO must be in the Active Directory  and the copy creates a new destination GPO. For more information about copying GPOs, see 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-copyto">IGPMGPO::CopyTo</a>.</div>
<div> </div>
Note that you must check the code returned by the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmresult-overallstatus">IGPMResult::OverallStatus</a> method as well as the one returned by this method to determine whether or not the operation succeeded. 
<b>OverallStatus</b> returns an overall status code for the operation. If no error occurred during the operation, it returns a success code; otherwise it returns a failure code.

For more information about security groups, see 
<a href="/windows/desktop/AD/how-security-groups-are-used-in-access-control">How Security Groups are Used in Access Control</a> in the Active Directory Programmer's Guide.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a>
---
UID: NF:gpmgmt.IGPMGPO.CopyTo
title: IGPMGPO::CopyTo (gpmgmt.h)
description: Copies the current Group Policy object (GPO) to the specified domain and then returns a pointer to the copy of the GPO.
helpviewer_keywords: ["CopyTo","CopyTo method [GPMC]","CopyTo method [GPMC]","GPMGPO object","CopyTo method [GPMC]","IGPMGPO interface","GPMGPO object [GPMC]","CopyTo method","IGPMGPO interface [GPMC]","CopyTo method","IGPMGPO.CopyTo","IGPMGPO::CopyTo","_win32_igpmgpo_copyto","gpmc.igpmgpo_copyto","gpmgmt/IGPMGPO::CopyTo"]
old-location: gpmc\igpmgpo_copyto.htm
tech.root: gpmc
ms.assetid: 17f4c6b2-6c75-4d4c-88c5-6d9ef2cb7a07
ms.date: 12/05/2018
ms.keywords: CopyTo, CopyTo method [GPMC], CopyTo method [GPMC],GPMGPO object, CopyTo method [GPMC],IGPMGPO interface, GPMGPO object [GPMC],CopyTo method, IGPMGPO interface [GPMC],CopyTo method, IGPMGPO.CopyTo, IGPMGPO::CopyTo, _win32_igpmgpo_copyto, gpmc.igpmgpo_copyto, gpmgmt/IGPMGPO::CopyTo
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
 - IGPMGPO::CopyTo
 - gpmgmt/IGPMGPO::CopyTo
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
 - IGPMGPO.CopyTo
 - GPMGPO.CopyTo
---

## -description

Copies the current Group Policy object (GPO) to the specified domain and then returns a pointer to the copy of 
    the GPO. This method copies the policy settings from the current GPO to the new GPO. The new GPO has a new GPO ID. 
    The new GPO gets either the default GPO 
    <a href="/windows/desktop/SecAuthZ/access-control-lists">access control lists</a> (ACLs) or the ACLs from the 
    source GPO. The ACL that the new GPO gets depends on the value of the <i>lFlags</i> parameter. 
    This method does not link any scopes of management (SOMs) to the new GPO.

## -parameters

### -param lFlags [in]

Specifies the options to use for security principal and path mapping. For more information, see 
      <a href="/previous-versions/windows/desktop/gpmc/copying-and-importing-gpos-across-domains">Copying and Importing GPOs Across Domains</a>. 
      The following options are defined.

#### 0

Map the security principal and the Universal Naming Convention (UNC) path from the migration table if 
        specified. If there is no entry corresponding to Security principal or UNCPath, keep the setting that contains the Security principal or UNC Path as it is. Do not copy security on the GPO and Software Installation Package objects. This is the default value of this parameter.

#### GPM_MIGRATIONTABLE_ONLY

Map the security principals and the UNC paths by using the information specified in the migration table 
        only. If a setting is found that cannot be mapped through the migration table, the method fails and returns an 
        error code.

#### GPM_PROCESS_SECURITY

Copy the specified permissions (DACLs) on the GPO.

### -param pIGPMDomain [in]

Domain to which the GPO is copied.

### -param pvarNewDisplayName [in, optional]

Display name for the copied GPO. A display name is assigned if the <b>VARIANT</b> structure does not contain a <b>BSTR</b> or if the <i>pvarNewDisplayName</i> parameter is <b>NULL</b>.

### -param pvarMigrationTable [in, optional]

Pointer to the <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmmigrationtable">IGPMMigrationTable</a> interface to use for mapping. This parameter can be <b>NULL</b>.

### -param pvarGPMProgress [in, optional]

Specifies a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasyncprogress">IGPMAsyncProgress</a> interface. This interface allows the client to receive status notifications about the progress of the copy operation. This parameter must be <b>NULL</b> if the client does not receive asynchronous notifications.

### -param pvarGPMCancel [out, optional]

Receives a pointer to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmasynccancel">IGPMAsyncCancel</a> interface that the client can use to cancel the copy operation. This parameter is not returned if <i>pvarGPMProgress</i> is <b>NULL</b>.

### -param ppIGPMResult [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a> interface that represents the result of the copy operation. That interface contains pointers to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a> interface and to an 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">GPMResult</a> object.

## -remarks

The new GPO that is created by using this method is unlinked because a copy operation does not transfer links.

You must check the code that is returned by the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmresult-overallstatus">IGPMResult::OverallStatus</a> method as well as the one returned by this method to determine whether the operation succeeded. 
<b>OverallStatus</b> returns an overall status code for the operation. If no error occurred during the operation, it returns a success code. Otherwise, it returns a failure code.

An import operation is similar to a copy operation, except that in an import operation, the source GPO must be in the file system and the destination must be an existing GPO in Active Directory. In contrast, for a copy operation, the source GPO must be in Active Directory. A copy operation creates a new destination GPO. An import operation transfers only policy settings. An import operation does not modify the GPO ID or the 
<a href="/windows/desktop/SecAuthZ/access-control-lists">ACLs</a> on the destination GPO. And, an import operation does not modify any links that point to the destination GPO or to an associated Windows Management Instrumentation (WMI) filter. For more information about importing GPOs, see 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmgpo-import">IGPMGPO::Import</a>.

For more information about security groups, see 
<a href="/windows/desktop/AD/how-security-groups-are-used-in-access-control">How Security Groups are Used in Access Control</a> in the Active Directory Programmer's Guide.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmdomain">IGPMDomain</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmresult">IGPMResult</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmstatusmsgcollection">IGPMStatusMsgCollection</a>
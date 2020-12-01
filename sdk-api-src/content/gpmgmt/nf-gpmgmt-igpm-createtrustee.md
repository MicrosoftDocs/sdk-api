---
UID: NF:gpmgmt.IGPM.CreateTrustee
title: IGPM::CreateTrustee (gpmgmt.h)
description: Creates and returns a GPMTrustee from which you can retrieve information about a trustee.
helpviewer_keywords: ["CreateTrustee","CreateTrustee method [GPMC]","CreateTrustee method [GPMC]","GPM object","CreateTrustee method [GPMC]","IGPM interface","GPM object [GPMC]","CreateTrustee method","IGPM interface [GPMC]","CreateTrustee method","IGPM.CreateTrustee","IGPM::CreateTrustee","_win32_igpm_createtrustee","gpmc.igpm_createtrustee","gpmgmt/IGPM::CreateTrustee"]
old-location: gpmc\igpm_createtrustee.htm
tech.root: gpmc
ms.assetid: 98230e5f-b866-4f68-9977-eec4bdd14d9e
ms.date: 12/05/2018
ms.keywords: CreateTrustee, CreateTrustee method [GPMC], CreateTrustee method [GPMC],GPM object, CreateTrustee method [GPMC],IGPM interface, GPM object [GPMC],CreateTrustee method, IGPM interface [GPMC],CreateTrustee method, IGPM.CreateTrustee, IGPM::CreateTrustee, _win32_igpm_createtrustee, gpmc.igpm_createtrustee, gpmgmt/IGPM::CreateTrustee
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
 - IGPM::CreateTrustee
 - gpmgmt/IGPM::CreateTrustee
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
 - IGPM.CreateTrustee
 - GPM.CreateTrustee
---

# IGPM::CreateTrustee


## -description

Creates and returns a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmtrustee">GPMTrustee</a> from which you can retrieve information about a trustee. A trustee is a user, computer, or security group that can be granted permissions on a Group Policy object (GPO), scope of management (SOM), or Windows Management Instrumentation (WMI) filter.

## -parameters

### -param bstrTrustee [in]

Required. Trustee name or the security identifier (SID). Names are in a format that is compatible with Security Accounts Manager (SAM), such as <i>Exampledomain</i>&#92;<i>Someone</i>.

### -param ppIGPMTrustee [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmtrustee">IGPMTrustee</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmtrustee">GPMTrustee</a> object.

<h3>VB</h3>
Returns a reference to a <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmtrustee">GPMTrustee</a> object.

## -remarks

For more information about policy-related permissions, see 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-createpermission">IGPM::CreatePermission</a>. For more information about security groups, see 
<a href="/windows/desktop/AD/how-security-groups-are-used-in-access-control">How Security Groups are Used in Access Control</a> in the Active Directory Programmer's Guide.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">IGPMPermission</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmtrustee">IGPMTrustee</a>
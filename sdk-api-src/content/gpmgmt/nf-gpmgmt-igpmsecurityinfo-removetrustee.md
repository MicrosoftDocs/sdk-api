---
UID: NF:gpmgmt.IGPMSecurityInfo.RemoveTrustee
title: IGPMSecurityInfo::RemoveTrustee (gpmgmt.h)
description: Removes all policy-related permissions for the specified trustee. A trustee is a user, computer, or security group that can be granted permissions on a GPO, SOM, or WMI filter.
helpviewer_keywords: ["GPMSecurityInfo class [GPMC]","RemoveTrustee method","IGPMSecurityInfo interface [GPMC]","RemoveTrustee method","IGPMSecurityInfo.RemoveTrustee","IGPMSecurityInfo::RemoveTrustee","RemoveTrustee","RemoveTrustee method [GPMC]","RemoveTrustee method [GPMC]","GPMSecurityInfo class","RemoveTrustee method [GPMC]","IGPMSecurityInfo interface","_win32_igpmsecurityinfo_removetrustee","gpmc.igpmsecurityinfo_removetrustee","gpmgmt/IGPMSecurityInfo::RemoveTrustee"]
old-location: gpmc\igpmsecurityinfo_removetrustee.htm
tech.root: gpmc
ms.assetid: e290648d-f480-4834-93a3-4759da581611
ms.date: 12/05/2018
ms.keywords: GPMSecurityInfo class [GPMC],RemoveTrustee method, IGPMSecurityInfo interface [GPMC],RemoveTrustee method, IGPMSecurityInfo.RemoveTrustee, IGPMSecurityInfo::RemoveTrustee, RemoveTrustee, RemoveTrustee method [GPMC], RemoveTrustee method [GPMC],GPMSecurityInfo class, RemoveTrustee method [GPMC],IGPMSecurityInfo interface, _win32_igpmsecurityinfo_removetrustee, gpmc.igpmsecurityinfo_removetrustee, gpmgmt/IGPMSecurityInfo::RemoveTrustee
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
 - IGPMSecurityInfo::RemoveTrustee
 - gpmgmt/IGPMSecurityInfo::RemoveTrustee
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
 - IGPMSecurityInfo.RemoveTrustee
 - GPMSecurityInfo.RemoveTrustee
---

# IGPMSecurityInfo::RemoveTrustee


## -description

Removes all policy-related permissions for the specified trustee. A trustee is a user, computer, or security group that can be granted permissions on a GPO, SOM, or WMI filter.

## -parameters

### -param bstrTrustee [in]

Required. The name or SID of the trustee for which all permissions should be removed. Names are in Security Accounts Manager (SAM) compatible format (Exampledomain\Someone). Use null-terminated string.

## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -remarks

On successful removal of a permission, the method updates all enumerators returned by the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmsecurityinfo-get__newenum">get__NewEnum</a> method, even if a removal occurs during the enumeration of elements.

For more information about policy-related permissions, see 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-createpermission">IGPM::CreatePermission</a>. For more information about security groups, see 
<a href="/windows/desktop/AD/how-security-groups-are-used-in-access-control">How Security Groups are Used in Access Control</a> in the Active Directory Programmer's Guide.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">IGPMPermission</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmtrustee">IGPMTrustee</a>
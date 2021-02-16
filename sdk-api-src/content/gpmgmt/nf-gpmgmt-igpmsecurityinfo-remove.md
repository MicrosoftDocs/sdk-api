---
UID: NF:gpmgmt.IGPMSecurityInfo.Remove
title: IGPMSecurityInfo::Remove (gpmgmt.h)
description: Removes the permission specified in a given GPMPermission object from the GPMSecurityInfo collection.
helpviewer_keywords: ["GPMSecurityInfo class [GPMC]","Remove method","IGPMSecurityInfo interface [GPMC]","Remove method","IGPMSecurityInfo.Remove","IGPMSecurityInfo::Remove","Remove","Remove method [GPMC]","Remove method [GPMC]","GPMSecurityInfo class","Remove method [GPMC]","IGPMSecurityInfo interface","_win32_igpmsecurityinfo_remove","gpmc.igpmsecurityinfo_remove","gpmgmt/IGPMSecurityInfo::Remove"]
old-location: gpmc\igpmsecurityinfo_remove.htm
tech.root: gpmc
ms.assetid: 187ae17c-82c0-4439-8b98-52ba0571d222
ms.date: 12/05/2018
ms.keywords: GPMSecurityInfo class [GPMC],Remove method, IGPMSecurityInfo interface [GPMC],Remove method, IGPMSecurityInfo.Remove, IGPMSecurityInfo::Remove, Remove, Remove method [GPMC], Remove method [GPMC],GPMSecurityInfo class, Remove method [GPMC],IGPMSecurityInfo interface, _win32_igpmsecurityinfo_remove, gpmc.igpmsecurityinfo_remove, gpmgmt/IGPMSecurityInfo::Remove
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
 - IGPMSecurityInfo::Remove
 - gpmgmt/IGPMSecurityInfo::Remove
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
 - IGPMSecurityInfo.Remove
 - GPMSecurityInfo.Remove
---

## -description

Removes the permission specified in a given 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">GPMPermission</a> object from the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">GPMSecurityInfo</a> collection.

## -parameters

### -param pPerm [in]

Pointer to the <b>GPMPermission</b> object to remove from the collection.

## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -remarks

You cannot remove Inherited permissions. To determine if a permission is Inherited, see 
<a href="/previous-versions/windows/desktop/gpmc/igpmpermission-property-methods">IGPMPermission Property Methods</a>.

The method checks for the existence of the specified <b>GPMPermission</b> object, which is the pairing of a trustee (which is a user, computer, or security group) and a permission that applies to a single object, for example, to a GPO, SOM, or WMI filter. If the object exists in the collection, the method removes it.

If the permission specified for removal represents a higher level than the permission that exists for the trustee, the method removes the lower level permission. An example of this situation is specifying the removal of the permGPOEditSecurityAndDelete permission when the trustee has the lower permGPOEdit permission instead. In this case, the method removes the permGPOEdit permission.

If the permission specified for removal represents a lower level than the permission that exists for the trustee, the method returns S_FALSE.

On successful removal of a permission, the method updates all enumerators returned by the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmsecurityinfo-get__newenum">get__NewEnum</a> method, even if a removal occurs during the enumeration of elements.

For more information about policy-related permissions, see 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-createpermission">IGPM::CreatePermission</a>.

For more information about security groups, see 
<a href="/windows/desktop/AD/how-security-groups-are-used-in-access-control">How Security Groups are Used in Access Control</a> in the Active Directory Programmer's Guide.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">IGPMPermission</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmtrustee">IGPMTrustee</a>
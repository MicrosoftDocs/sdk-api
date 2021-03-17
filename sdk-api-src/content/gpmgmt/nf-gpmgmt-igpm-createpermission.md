---
UID: NF:gpmgmt.IGPM.CreatePermission
title: IGPM::CreatePermission (gpmgmt.h)
description: Creates and returns an interface or object that represents the trustee (such as a user, computer or security group) and permission that applies to a single object; for example, to a GPO, SOM or a WMI filter.
helpviewer_keywords: ["CreatePermission","CreatePermission method [GPMC]","CreatePermission method [GPMC]","GPM object","CreatePermission method [GPMC]","IGPM interface","GPM object [GPMC]","CreatePermission method","IGPM interface [GPMC]","CreatePermission method","IGPM.CreatePermission","IGPM::CreatePermission","_win32_igpm_createpermission","gpmc.igpm_createpermission","gpmgmt/IGPM::CreatePermission","permGPOApply","permGPOEdit","permGPOEditSecurityAndDelete","permGPORead","permSOMGPOCreate","permSOMLink","permSOMLogging","permSOMPlanning","permSOMWMICreate","permSOMWMIFullControl","permWMIFilterEdit","permWMIFilterFullControl"]
old-location: gpmc\igpm_createpermission.htm
tech.root: gpmc
ms.assetid: 8da90ca3-1c81-414f-b1a0-a0dfcae745ba
ms.date: 12/05/2018
ms.keywords: CreatePermission, CreatePermission method [GPMC], CreatePermission method [GPMC],GPM object, CreatePermission method [GPMC],IGPM interface, GPM object [GPMC],CreatePermission method, IGPM interface [GPMC],CreatePermission method, IGPM.CreatePermission, IGPM::CreatePermission, _win32_igpm_createpermission, gpmc.igpm_createpermission, gpmgmt/IGPM::CreatePermission, permGPOApply, permGPOEdit, permGPOEditSecurityAndDelete, permGPORead, permSOMGPOCreate, permSOMLink, permSOMLogging, permSOMPlanning, permSOMWMICreate, permSOMWMIFullControl, permWMIFilterEdit, permWMIFilterFullControl
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
 - IGPM::CreatePermission
 - gpmgmt/IGPM::CreatePermission
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
 - IGPM.CreatePermission
 - GPM.CreatePermission
---

# IGPM::CreatePermission


## -description

Creates and returns an interface or object that represents the trustee (such as a user, computer or security group) and permission that applies to a single object; for example, to a GPO, SOM or a WMI filter.

## -parameters

### -param bstrTrustee [in]

Required. Trustee name. This parameter can be a string that specifies the security identifier (SID) of the account. This parameter can also be a Security Accounts Manager (SAM) account name, such as "Engineering\JSmith".

### -param perm [in]

Required. Permission to use for the trustee. The following policy-related permissions are supported. Note that each permission value represents one or more 
<a href="/windows/desktop/SecAuthZ/access-rights-and-access-masks">access rights</a> that apply to the GPO.

The following GPO permissions are supported.



#### permGPOApply

The trustee can apply the GPO. This value corresponds to the READ and APPLY Group Policy access rights being set to Allow for a user.



#### permGPORead

The trustee can read the GPO. This value corresponds to the READ Group Policy access right being set to Allow for a user.



#### permGPOEdit

The trustee can read and edit the policy settings for the GPO. This value corresponds to the READ, WRITE, CREATE CHILD OBJECT, and DELETE CHILD OBJECT Group Policy access rights being set to Allow for a user.



#### permGPOEditSecurityAndDelete

The trustee can read, edit and delete the permissions for the GPO. This value corresponds to the Group Policy access rights specified by <b>permGPOEdit</b> plus the DELETE, MODIFY PERMISSIONS, and MODIFY OWNER access rights being set to Allow for a user.

The following WMI filter permissions are supported.



#### permWMIFilterEdit

The trustee can edit the WMI filter.



#### permWMIFilterFullControl

The trustee has full control over the WMI filter.

The following scope of management (SOM) permissions are supported.



#### permSOMLink

The trustee can link GPOs to the SOM. Applies to sites, domains and OUs.



#### permSOMLogging

The trustee can generate RSoP logging data for the SOM. Applies to domains and OUs.



#### permSOMPlanning

The trustee can generate RSoP planning data for the SOM. Applies to domains and OUs.



#### permSOMWMICreate

The trustee can create WMI filters in the domain. Applies to domains only.



#### permSOMWMIFullControl

The trustee has full control over all the WMI filters in the domain. Applies to domains only.



#### permSOMGPOCreate

The trustee can create GPOs in the domain. Applies to domains only.

### -param bInheritable [in]

<table>
<tr>
<td><strong>C++</strong></td>
<td>
<b>VARIANT_BOOL</b>. If <b>VARIANT_TRUE</b>, children inherit the permission. Note that this parameter is significant only when you add permissions to security information using the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmsecurityinfo-add">IGPMSecurityInfo::Add</a> method. This parameter is ignored for searches.

</td>
</tr>
<tr>
<td><strong>JScript</strong></td>
<td>
If true, children inherit the permission. Note that this parameter is significant only when you add permissions to security information using the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmsecurityinfo-add">GPMSecurityInfo.Add</a> method. This parameter is ignored for searches.

</td>
</tr>
</table>

### -param ppPerm [out]

Address of a pointer to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">IGPMPermission</a> interface.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMPermission</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMPermission</b> object.

## -remarks

For more information about access control lists (ACLs), access rights, and the security model for controlling access to Windows objects, see <a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>. For more information about security groups, see 
How <a href="/windows/desktop/AD/how-security-groups-are-used-in-access-control">Security Groups are Used in Access Control</a> in the Active Directory Programmer's Guide.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">IGPMPermission</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmtrustee">IGPMTrustee</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>
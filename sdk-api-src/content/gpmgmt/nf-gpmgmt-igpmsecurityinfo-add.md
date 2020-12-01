---
UID: NF:gpmgmt.IGPMSecurityInfo.Add
title: IGPMSecurityInfo::Add (gpmgmt.h)
description: Adds the permission specified in a GPMPermission object to the GPMSecurityInfo collection. You can add a permission that is above the level of existing permissions. For more information about restrictions that apply, see the following Remarks section.
helpviewer_keywords: ["Add","Add method [GPMC]","Add method [GPMC]","GPMSecurityInfo class","Add method [GPMC]","IGPMSecurityInfo interface","GPMSecurityInfo class [GPMC]","Add method","IGPMSecurityInfo interface [GPMC]","Add method","IGPMSecurityInfo.Add","IGPMSecurityInfo::Add","_win32_igpmsecurityinfo_add","gpmc.igpmsecurityinfo_add","gpmgmt/IGPMSecurityInfo::Add"]
old-location: gpmc\igpmsecurityinfo_add.htm
tech.root: gpmc
ms.assetid: d180a4ed-7c7d-4df9-a2a4-7aab46446283
ms.date: 12/05/2018
ms.keywords: Add, Add method [GPMC], Add method [GPMC],GPMSecurityInfo class, Add method [GPMC],IGPMSecurityInfo interface, GPMSecurityInfo class [GPMC],Add method, IGPMSecurityInfo interface [GPMC],Add method, IGPMSecurityInfo.Add, IGPMSecurityInfo::Add, _win32_igpmsecurityinfo_add, gpmc.igpmsecurityinfo_add, gpmgmt/IGPMSecurityInfo::Add
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
 - IGPMSecurityInfo::Add
 - gpmgmt/IGPMSecurityInfo::Add
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
 - IGPMSecurityInfo.Add
 - GPMSecurityInfo.Add
---

## -description

Adds the permission specified in a 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">GPMPermission</a> object to the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">GPMSecurityInfo</a> collection. You can add a permission that is above the level of existing permissions. For more information about restrictions that apply, see the following Remarks section.

## -parameters

### -param pPerm [in]

Pointer to the <b>GPMPermission</b> object to add to the collection.

## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -remarks

A trustee is a user, computer, or security group that can be granted permissions on a GPO, SOM, or WMI filter.

Note that there can be some overlap of the permission levels that apply to a given object. Instances include the following:

<ul>
<li>permGPOEditSecurity is a superset of permGPOEdit, which is a superset of permGPORead</li>
<li>permGPOApply is a superset of permGPORead</li>
<li>permWMIFilterFullControl is a superset of permWMIFilterEdit</li>
<li>permSOMWMIFullControl is a superset of permSOMWMICreate</li>
</ul>
If a permission that you are adding for a trustee overlaps (as defined above) with an existing permission that already exists on the object, the following rules apply:

<ol>
<li>If there is an Inherited permission on the object, you cannot add a higher level permission for the user. This is because an Inherited permission cannot be modified. The permission must first be removed from the parent container before a change can be made to the Inherited permission.</li>
<li>If there is a Denied permission on the object, you cannot add a higher level permission to the existing permission for the user.</li>
<li>If there is a permission that is explicitly set on the object, adding a lower level permission does not change the user's permissions. In addition, the method returns S_FALSE, which can be tested for by the calling application.</li>
<li>If there is a permission that is explicitly set on the object, adding a higher level permission changes the user's permissions.</li>
<li>Because permGPORead is a subset of permGPOEdit and permGPOApply, permGPORead can be removed only if both permGPOEdit and permGPOApply are removed.</li>
<li>If the current permission is not inheritable, and the permission you are adding sets the Inheritable property to TRUE, then the permission is changed to be an inheritable one.</li>
<li>If the current permission is inheritable, and the permission you are adding sets the Inheritable property to FALSE, the method returns S_FALSE.</li>
</ol>
Note that you cannot add Denied, Inherited, or custom permissions using the GPMC, but you can add Inheritable permissions. You can delete Denied and custom permissions. If you attempt to add a Denied permission, it results in an error. Custom permissions are those that do not match any of the permission levels defined by the GPMC. For example, if a trustee is granted the "Apply" ACE for a GPO, but not the "Read" ACE, the permission is a custom permission. To determine if a permission is Denied or Inherited you can call the 
<a href="/previous-versions/windows/desktop/gpmc/igpmpermission-property-methods">IGPMPermission Property Methods</a>.

For more information about predefined policy-related permissions, see 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-createpermission">IGPM::CreatePermission</a>. For information about permission categories and levels, see 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a>.

When adding permissions on a GPO, the value of the Inheritable property is ignored and set to <b>TRUE</b>. This is because all GPO permissions should be inheritable to the User and Computer child containers in the directory service and to subdirectories in the system volume folder (SysVol). When adding permissions on WMI filters, the value of the Inheritable property is always set to <b>FALSE</b>.

For more information about security groups, see 
<a href="/windows/desktop/AD/how-security-groups-are-used-in-access-control">How Security Groups are Used in Access Control</a> in the Active Directory Programmer's Guide.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">IGPMPermission</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmtrustee">IGPMTrustee</a>
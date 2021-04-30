---
UID: NN:gpmgmt.IGPMPermission
title: IGPMPermission (gpmgmt.h)
description: The IGPMPermission interface contains methods to retrieve permission-related properties when using the GPMC.
helpviewer_keywords: ["GPMPermission","IGPMPermission","IGPMPermission interface [GPMC]","IGPMPermission interface [GPMC]","described","_win32_igpmpermission","gpmc.igpmpermission","gpmgmt/IGPMPermission"]
old-location: gpmc\igpmpermission.htm
tech.root: gpmc
ms.assetid: 7ac19065-571e-45f5-934f-35ddbf225262
ms.date: 12/05/2018
ms.keywords: GPMPermission, IGPMPermission, IGPMPermission interface [GPMC], IGPMPermission interface [GPMC],described, _win32_igpmpermission, gpmc.igpmpermission, gpmgmt/IGPMPermission
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
 - IGPMPermission
 - gpmgmt/IGPMPermission
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
 - IGPMPermission
 - GPMPermission
---

# IGPMPermission interface


## -description

The 
<b>IGPMPermission</b> interface contains methods to retrieve permission-related properties when using the GPMC. The <b>GPMPermission</b> object represents the pairing of a trustee (such as a user or security group) and a policy-related permission that applies to a single object; for example, to a GPO or a WMI filter. To create a <b>GPMPermission</b> object, call the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-createpermission">IGPM::CreatePermission</a> method.

## -remarks

The interface divides the policy-related permissions into categories. The following table lists the categories, permissions included in the categories, and the object to which they can be applied, as  defined in the GPMPermissionType.

<table>
<tr>
<th>Securable object</th>
<th>Permission category</th>
<th>Permission level</th>
</tr>
<tr>
<td>
Site

</td>
<td>
GPO linking

</td>
<td>
permSOMLink

</td>
</tr>
<tr>
<td>
OU

</td>
<td>
GPO linking

</td>
<td>
permSOMLink

</td>
</tr>
<tr>
<td></td>
<td>
RSoP logging

</td>
<td>
permSOMLogging

</td>
</tr>
<tr>
<td></td>
<td>
RSoP planning

</td>
<td>
permSOMPlanning

</td>
</tr>
<tr>
<td>
Domain

</td>
<td>
GPO linking

</td>
<td>
permSOMLink

</td>
</tr>
<tr>
<td></td>
<td>
Creating GPOs

</td>
<td>
permSOMGPOCreate

</td>
</tr>
<tr>
<td></td>
<td>
RSoP logging

</td>
<td>
permSOMLogging

</td>
</tr>
<tr>
<td></td>
<td>
RSoP planning

</td>
<td>
permSOMPlanning

</td>
</tr>
<tr>
<td></td>
<td>
Creating WMI filters

</td>
<td>
permSOMWMICreate

</td>
</tr>
<tr>
<td></td>
<td></td>
<td>
permSOMWMIFullControl

</td>
</tr>
<tr>
<td>
WMI filter

</td>
<td>
Editing WMI filters

</td>
<td>
permWMIFilterEdit

</td>
</tr>
<tr>
<td></td>
<td>
Full control of all WMI filters

</td>
<td>
permWMIFilterFullControl

</td>
</tr>
<tr>
<td></td>
<td>
Custom control of WMI filters

</td>
<td>
permWMIFilterCustom

</td>
</tr>
<tr>
<td>
GPO

</td>
<td>
Security filtering

</td>
<td>
permGPOApply

</td>
</tr>
<tr>
<td></td>
<td>
Delegation

</td>
<td>
permGPORead

</td>
</tr>
<tr>
<td></td>
<td></td>
<td>
permGPOEdit

</td>
</tr>
<tr>
<td></td>
<td></td>
<td>
permGPOEditSecurityAndDelete

</td>
</tr>
<tr>
<td></td>
<td></td>
<td>
permGPOCustom

</td>
</tr>
<tr>
<td>
Starter GPO

</td>
<td>
Delegation

</td>
<td>
permStarterGPORead

</td>
</tr>
<tr>
<td></td>
<td></td>
<td>
permStarterGPOEdit

</td>
</tr>
<tr>
<td></td>
<td></td>
<td>
permStarterGPOFullControl

</td>
</tr>
<tr>
<td></td>
<td></td>
<td>
permStarterGPOCustom

</td>
</tr>
<tr>
<td></td>
<td></td>
<td>
permSOMStarterGPOCreate

</td>
</tr>
</table>
 

For more information about predefined policy-related permissions, see 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-createpermission">IGPM::CreatePermission</a> (<b>GPM.CreatePermission</b>).

For more information about security groups, see 
<a href="/windows/desktop/AD/how-security-groups-are-used-in-access-control">How Security Groups are Used in Access Control</a> in the Active Directory Programmer's Guide.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsecurityinfo">IGPMSecurityInfo</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmtrustee">IGPMTrustee</a>
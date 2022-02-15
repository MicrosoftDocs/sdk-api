---
UID: NN:gpmgmt.IGPMSecurityInfo
title: IGPMSecurityInfo (gpmgmt.h)
description: The IGPMSecurityInfo interface defines the methods of the GPMSecurityInfo collection. This collection represents a set of policy-related permissions that can be set on a particular object, such as a scope of management (SOM), a GPO, or a WMI filter.
helpviewer_keywords: ["GPMSecurityInfo","IGPMSecurityInfo","IGPMSecurityInfo interface [GPMC]","IGPMSecurityInfo interface [GPMC]","described","_win32_igpmsecurityinfo","gpmc.igpmsecurityinfo","gpmgmt/IGPMSecurityInfo"]
old-location: gpmc\igpmsecurityinfo.htm
tech.root: gpmc
ms.assetid: 1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74
ms.date: 12/05/2018
ms.keywords: GPMSecurityInfo, IGPMSecurityInfo, IGPMSecurityInfo interface [GPMC], IGPMSecurityInfo interface [GPMC],described, _win32_igpmsecurityinfo, gpmc.igpmsecurityinfo, gpmgmt/IGPMSecurityInfo
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
 - IGPMSecurityInfo
 - gpmgmt/IGPMSecurityInfo
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
 - IGPMSecurityInfo
 - IGPMSecurityInfo.Item
 - IGPMSecurityInfo.get_Item
 - GPMSecurityInfo
---

# IGPMSecurityInfo interface


## -description

The <b>IGPMSecurityInfo</b> interface defines the methods of 
    the <b>GPMSecurityInfo</b> collection. This collection 
    represents a set of policy-related permissions that can be set on a particular object, such as a scope of 
    management (SOM), a GPO, or a WMI filter.

## -inheritance

The <b>IGPMSecurityInfo</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMSecurityInfo</b> also has these types of members:

## -remarks

The interface divides the policy-related permissions into categories. The following table lists the categories, 
     permissions included in the categories, and the object to which they can be applied.

<table>
<tr>
<th>Securable object</th>
<th>Permission category</th>
<th>Permission level</th>
</tr>
<tr>
<td>Site</td>
<td>GPO linking</td>
<td>permSOMLink</td>
</tr>
<tr>
<td>OU</td>
<td>GPO linking</td>
<td>permSOMLink</td>
</tr>
<tr>
<td></td>
<td>RSoP logging</td>
<td>permSOMLogging</td>
</tr>
<tr>
<td></td>
<td>RSoP planning</td>
<td>permSOMPlanning</td>
</tr>
<tr>
<td>Domain</td>
<td>GPO linking</td>
<td>permSOMLink</td>
</tr>
<tr>
<td></td>
<td>Creating GPOs</td>
<td>permSOMGPOCreate</td>
</tr>
<tr>
<td></td>
<td>RSoP logging</td>
<td>permSOMLogging</td>
</tr>
<tr>
<td></td>
<td>RSoP planning</td>
<td>permSOMPlanning</td>
</tr>
<tr>
<td></td>
<td>Creating WMI filters</td>
<td>permSOMWMICreate</td>
</tr>
<tr>
<td></td>
<td></td>
<td>permSOMWMIFullControl</td>
</tr>
<tr>
<td>WMI filter</td>
<td>Editing WMI filters</td>
<td>permWMIFilterEdit</td>
</tr>
<tr>
<td></td>
<td>Full control of all WMI filters</td>
<td>permWMIFilterFullControl</td>
</tr>
<tr>
<td></td>
<td>Custom control of WMI filters</td>
<td>permWMIFilterCustom</td>
</tr>
<tr>
<td>GPO</td>
<td>Security filtering</td>
<td>permGPOApply</td>
</tr>
<tr>
<td></td>
<td>Delegation</td>
<td>permGPORead</td>
</tr>
<tr>
<td></td>
<td></td>
<td>permGPOEdit</td>
</tr>
<tr>
<td></td>
<td></td>
<td>permGPOEditSecurityAndDelete</td>
</tr>
<tr>
<td></td>
<td></td>
<td>permGPOCustom</td>
</tr>
</table>
 

The <b>GPMSecurityInfo</b> collection represents a 
    collection of <a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">GPMPermission</a> objects for a particular SOM, 
    GPO, or WMI filter. Note however, that although the 
    <b>GPMSecurityInfo</b> object is a collection object, it is not 
    a typical collection object. This is because no action occurs if the 
    <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmsecurityinfo-add">Add</a> method attempts to add a 
    <b>GPMPermission</b> object for a trustee and the permission is 
    below the level of an existing permission for that trustee. For more information, see the 
    <b>Add</b> method.

For more information about policy-related permissions, see 
    <a href="/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-createpermission">IGPM::CreatePermission</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmpermission">IGPMPermission</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmtrustee">IGPMTrustee</a>

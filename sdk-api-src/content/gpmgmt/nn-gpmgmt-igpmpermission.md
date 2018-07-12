---
UID: NN:gpmgmt.IGPMPermission
title: IGPMPermission
author: windows-sdk-content
description: The IGPMPermission interface contains methods to retrieve permission-related properties when using the GPMC.
old-location: gpmc\igpmpermission.htm
old-project: gpmc
ms.assetid: 7ac19065-571e-45f5-934f-35ddbf225262
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: GPMPermission, IGPMPermission, IGPMPermission interface [GPMC], IGPMPermission interface [GPMC],described, _win32_igpmpermission, gpmc.igpmpermission, gpmgmt/IGPMPermission
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: GPMStarterGPOType
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
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMPermission interface


## -description


The 
<b>IGPMPermission</b> interface contains methods to retrieve permission-related properties when using the GPMC. The <b>GPMPermission</b> object represents the pairing of a trustee (such as a user or security group) and a policy-related permission that applies to a single object; for example, to a GPO or a WMI filter. To create a <b>GPMPermission</b> object, call the 
<a href="https://msdn.microsoft.com/8da90ca3-1c81-414f-b1a0-a0dfcae745ba">IGPM::CreatePermission</a> method.


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
<a href="https://msdn.microsoft.com/8da90ca3-1c81-414f-b1a0-a0dfcae745ba">IGPM::CreatePermission</a> (<b>GPM.CreatePermission</b>).

For more information about security groups, see 
<a href="https://msdn.microsoft.com/3236c51f-21c1-4c07-9b76-2668ae72a42f">How Security Groups are Used in Access Control</a> in the Active Directory Programmer's Guide.




## -see-also




<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">IGPMSecurityInfo</a>



<a href="https://msdn.microsoft.com/f9c24fe6-58c7-4e82-9ac0-1157ed8fffeb">IGPMTrustee</a>
 

 


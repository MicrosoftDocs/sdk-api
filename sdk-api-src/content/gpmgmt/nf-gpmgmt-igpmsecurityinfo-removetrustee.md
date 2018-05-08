---
UID: NF:gpmgmt.IGPMSecurityInfo.RemoveTrustee
title: IGPMSecurityInfo::RemoveTrustee
author: windows-driver-content
description: Removes all policy-related permissions for the specified trustee. A trustee is a user, computer, or security group that can be granted permissions on a GPO, SOM, or WMI filter.
old-location: gpmc\igpmsecurityinfo_removetrustee.htm
old-project: GPMC
ms.assetid: e290648d-f480-4834-93a3-4759da581611
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GPMSecurityInfo class [GPMC],RemoveTrustee method, IGPMSecurityInfo interface [GPMC],RemoveTrustee method, IGPMSecurityInfo.RemoveTrustee, IGPMSecurityInfo::RemoveTrustee, RemoveTrustee, RemoveTrustee method [GPMC], RemoveTrustee method [GPMC],GPMSecurityInfo class, RemoveTrustee method [GPMC],IGPMSecurityInfo interface, _win32_igpmsecurityinfo_removetrustee, gpmc.igpmsecurityinfo_removetrustee, gpmgmt/IGPMSecurityInfo::RemoveTrustee
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPMSecurityInfo.RemoveTrustee
-	GPMSecurityInfo.RemoveTrustee
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
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
<a href="https://msdn.microsoft.com/f8dc2ee1-d1cb-4e7a-abf4-1a388320b681">get__NewEnum</a> method, even if a removal occurs during the enumeration of elements.

For more information about policy-related permissions, see 
<a href="https://msdn.microsoft.com/8da90ca3-1c81-414f-b1a0-a0dfcae745ba">IGPM::CreatePermission</a>. For more information about security groups, see 
<a href="https://msdn.microsoft.com/3236c51f-21c1-4c07-9b76-2668ae72a42f">How Security Groups are Used in Access Control</a> in the Active Directory Programmer's Guide.




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/7ac19065-571e-45f5-934f-35ddbf225262">IGPMPermission</a>



<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">IGPMSecurityInfo</a>



<a href="https://msdn.microsoft.com/f9c24fe6-58c7-4e82-9ac0-1157ed8fffeb">IGPMTrustee</a>
 

 


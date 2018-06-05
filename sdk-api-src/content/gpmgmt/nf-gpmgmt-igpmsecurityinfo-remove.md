---
UID: NF:gpmgmt.IGPMSecurityInfo.Remove
title: IGPMSecurityInfo::Remove
author: windows-sdk-content
description: Removes the permission specified in a given GPMPermission object from the GPMSecurityInfo collection.
old-location: gpmc\igpmsecurityinfo_remove.htm
old-project: GPMC
ms.assetid: 187ae17c-82c0-4439-8b98-52ba0571d222
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: GPMSecurityInfo class [GPMC],Remove method, IGPMSecurityInfo interface [GPMC],Remove method, IGPMSecurityInfo.Remove, IGPMSecurityInfo::Remove, Remove, Remove method [GPMC], Remove method [GPMC],GPMSecurityInfo class, Remove method [GPMC],IGPMSecurityInfo interface, _win32_igpmsecurityinfo_remove, gpmc.igpmsecurityinfo_remove, gpmgmt/IGPMSecurityInfo::Remove
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPMSecurityInfo.Remove
-	GPMSecurityInfo.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMSecurityInfo::Remove


## -description


Removes the permission specified in a given 
<a href="https://msdn.microsoft.com/7ac19065-571e-45f5-934f-35ddbf225262">GPMPermission</a> object from the 
<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">GPMSecurityInfo</a> collection.


## -parameters




### -param pPerm [in]

Pointer to the <b>GPMPermission</b> object to remove from the collection.


#### - objGPMPermission

<b>GPMPermission</b> object to remove.


## -returns



<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -remarks



You cannot remove Inherited permissions. To determine if a permission is Inherited, see 
<a href="https://msdn.microsoft.com/4af04405-66a4-4721-83ff-70ae505b3494">IGPMPermission Property Methods</a>.

The method checks for the existence of the specified <b>GPMPermission</b> object, which is the pairing of a trustee (which is a user, computer, or security group) and a permission that applies to a single object, for example, to a GPO, SOM, or WMI filter. If the object exists in the collection, the method removes it.

If the permission specified for removal represents a higher level than the permission that exists for the trustee, the method removes the lower level permission. An example of this situation is specifying the removal of the permGPOEditSecurityAndDelete permission when the trustee has the lower permGPOEdit permission instead. In this case, the method removes the permGPOEdit permission.

If the permission specified for removal represents a lower level than the permission that exists for the trustee, the method returns S_FALSE.

On successful removal of a permission, the method updates all enumerators returned by the 
<a href="https://msdn.microsoft.com/f8dc2ee1-d1cb-4e7a-abf4-1a388320b681">get__NewEnum</a> method, even if a removal occurs during the enumeration of elements.

For more information about policy-related permissions, see 
<a href="https://msdn.microsoft.com/8da90ca3-1c81-414f-b1a0-a0dfcae745ba">IGPM::CreatePermission</a>.

For more information about security groups, see 
<a href="https://msdn.microsoft.com/3236c51f-21c1-4c07-9b76-2668ae72a42f">How Security Groups are Used in Access Control</a> in the Active Directory Programmer's Guide.




## -see-also




<a href="https://msdn.microsoft.com/7ac19065-571e-45f5-934f-35ddbf225262">IGPMPermission</a>



<a href="https://msdn.microsoft.com/1205b1d7-3dc1-4ecd-b4fa-c833dd4e1a74">IGPMSecurityInfo</a>



<a href="https://msdn.microsoft.com/f9c24fe6-58c7-4e82-9ac0-1157ed8fffeb">IGPMTrustee</a>
 

 


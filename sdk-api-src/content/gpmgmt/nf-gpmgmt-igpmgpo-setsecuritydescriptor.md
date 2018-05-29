---
UID: NF:gpmgmt.IGPMGPO.SetSecurityDescriptor
title: IGPMGPO::SetSecurityDescriptor
author: windows-sdk-content
description: Sets the security descriptor for the GPO. The method replaces the existing security descriptor.
old-location: gpmc\igpmgpo_setsecuritydescriptor.htm
old-project: GPMC
ms.assetid: 087cbe19-25d9-4134-8893-1b2906915220
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: DACL_SECURITY_INFORMATION, GPMGPO class [GPMC],SetSecurityDescriptor method, GROUP_SECURITY_INFORMATION, IGPMGPO interface [GPMC],SetSecurityDescriptor method, IGPMGPO.SetSecurityDescriptor, IGPMGPO::SetSecurityDescriptor, OWNER_SECURITY_INFORMATION, SACL_SECURITY_INFORMATION, SetSecurityDescriptor, SetSecurityDescriptor method [GPMC], SetSecurityDescriptor method [GPMC],GPMGPO class, SetSecurityDescriptor method [GPMC],IGPMGPO interface, _win32_igpmgpo_setsecuritydescriptor, gpmc.igpmgpo_setsecuritydescriptor, gpmgmt/IGPMGPO::SetSecurityDescriptor
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
req.typenames: GPMStarterGPOType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpmgmt.dll
api_name:
-	IGPMGPO.SetSecurityDescriptor
-	GPMGPO.SetSecurityDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMGPO::SetSecurityDescriptor


## -description


Sets the security descriptor for the GPO. The method replaces the existing security descriptor.


## -parameters




### -param lFlags [in]

Specifies a set of bit flags. Use this parameter to specify the parts of the security descriptor to set.



#### OWNER_SECURITY_INFORMATION (1)

Owner identifier of the object.



#### GROUP_SECURITY_INFORMATION (2)

Primary group identifier.



#### DACL_SECURITY_INFORMATION (4)

Discretionary ACL of the object.



#### SACL_SECURITY_INFORMATION (8)

System ACL of the object.


### -param pSD [in]

The security descriptor to set.


#### - objIADsSecurityDescriptor


<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a> object to set.


## -returns



<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -remarks



For more information about ACLs and the security model for controlling access to Windows objects, see the 
<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a> topic .




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>



<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>
 

 


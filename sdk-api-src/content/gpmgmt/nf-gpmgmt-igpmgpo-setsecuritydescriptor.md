---
UID: NF:gpmgmt.IGPMGPO.SetSecurityDescriptor
title: IGPMGPO::SetSecurityDescriptor (gpmgmt.h)
author: windows-sdk-content
description: Sets the security descriptor for the GPO. The method replaces the existing security descriptor.
old-location: gpmc\igpmgpo_setsecuritydescriptor.htm
tech.root: gpmc
ms.assetid: 087cbe19-25d9-4134-8893-1b2906915220
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DACL_SECURITY_INFORMATION, GPMGPO class [GPMC],SetSecurityDescriptor method, GROUP_SECURITY_INFORMATION, IGPMGPO interface [GPMC],SetSecurityDescriptor method, IGPMGPO.SetSecurityDescriptor, IGPMGPO::SetSecurityDescriptor, OWNER_SECURITY_INFORMATION, SACL_SECURITY_INFORMATION, SetSecurityDescriptor, SetSecurityDescriptor method [GPMC], SetSecurityDescriptor method [GPMC],GPMGPO class, SetSecurityDescriptor method [GPMC],IGPMGPO interface, _win32_igpmgpo_setsecuritydescriptor, gpmc.igpmgpo_setsecuritydescriptor, gpmgmt/IGPMGPO::SetSecurityDescriptor
ms.topic: method
f1_keywords: 
 - "gpmgmt/IGPMGPO.SetSecurityDescriptor"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMGPO.SetSecurityDescriptor
 - GPMGPO.SetSecurityDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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


<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a> object to set.


## -returns



<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -remarks



For more information about ACLs and the security model for controlling access to Windows objects, see the 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-control">Access Control</a> topic .




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-control">Access Control</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>
 

 


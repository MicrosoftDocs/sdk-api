---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 


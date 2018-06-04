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

# QuerySecurityAccessMask function


## -description


The <b>QuerySecurityAccessMask</b> function creates an access mask that represents the access permissions necessary to query the specified object security information.


## -parameters




### -param SecurityInformation [in]

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a> structure that specifies the security information to be queried.


### -param DesiredAccess [out]

A pointer to the access mask that this function creates.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/764a4e93-0865-49f8-9b3a-1a178073454d">SetSecurityAccessMask</a>
 

 


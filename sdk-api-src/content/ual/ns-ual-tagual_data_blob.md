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

# tagUAL_DATA_BLOB structure


## -description


Specifies information about a User Access Logging (UAL) session.


## -struct-fields




### -field Size

The size, in bytes, of this structure.


### -field RoleGuid

A <a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a> structure that represents the role or minor product name associated with a UAL session.


### -field TenantId

A <a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a> structure that identifies a tenant of a hosted environment. This can be used to differentiate client tenants when more than one tenant uses the same host service.


### -field Address

The IP address of the client that accompanies the UAL payload from installed roles and products.


### -field UserName

The name of the client user that accompanies the UAL payload from installed roles and products..


## -see-also




<a href="https://msdn.microsoft.com/C7A0340F-3250-4570-9672-FC78AFC9ECC6">UalInstrument</a>



<a href="https://msdn.microsoft.com/800E8BCF-39A1-490A-9B6A-12EE900B8D17">UalStart</a>



<a href="https://msdn.microsoft.com/142A0C96-2D53-4C31-9847-D6D5313C841E">UalStop</a>
 

 


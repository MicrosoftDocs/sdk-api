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

# _USER_INFO_24 structure


## -description


The
				<b>USER_INFO_24</b> structure contains user account information on an account which is connected to an Internet identity. This information includes the Internet provider name for the user, the user's Internet name, and the user's security identifier (SID).


## -struct-fields




### -field usri24_internet_identity

A boolean value that indicates whether an account is connected to an Internet identity. 

This member is true if the account is connected  to an Internet identity. The other members in this structure can be used. 

If this member is false, then the account is not connected  to an Internet identity and other members in this structure should be ignored.


### -field usri24_flags

A set of flags. This member must be zero.


### -field usri24_internet_provider_name

A pointer to a Unicode string that specifies the Internet provider name. 


### -field usri24_internet_principal_name

A pointer to a Unicode string that specifies the user's Internet name. 


### -field usri24_user_sid

The local account SID of the user.


## -remarks



A user's account for logging onto Windows can be connected to an Internet identity. The user account can be a local account on a computer or a domain account for computers joined to a domain. The <b>USER_INFO_24</b> structure is used to provide information on an account which is connected to an Internet identity.

On Windows 8 and Windows Server 2012, the Internet identity for a connected account can often be used instead of the computer account.




## -see-also




<a href="https://msdn.microsoft.com/5bd13bed-938a-4273-840e-99fca99f7139">NetUserGetInfo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>
 

 


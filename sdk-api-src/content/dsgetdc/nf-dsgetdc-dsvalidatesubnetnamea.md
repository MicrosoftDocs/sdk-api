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

# DsValidateSubnetNameA function


## -description


The <b>DsValidateSubnetName</b> function validates a subnet name in the form xxx.xxx.xxx.xxx/YY. The Xxx.xxx.xxx.xxx portion must be a valid IP address. Yy must be the number of leftmost significant bits included in the mask. All bits of the IP address that are not covered by the mask must be specified as zero.


## -parameters




### -param SubnetName [in]

Pointer to a null-terminated string that specifies the name of the subnet to validate.


## -returns



If the function returns account information, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is the following error code.




## -see-also




<a href="https://msdn.microsoft.com/7b519c81-5a6c-470a-a525-1894efd53305">Directory Service Functions</a>



<a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a>



<a href="https://msdn.microsoft.com/2dfffd9a-af4f-4a93-8b3c-966e4f7c455f">DsGetSiteName</a>
 

 


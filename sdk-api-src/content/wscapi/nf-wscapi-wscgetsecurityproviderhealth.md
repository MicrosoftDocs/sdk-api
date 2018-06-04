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

# WscGetSecurityProviderHealth function


## -description


Gets the aggregate health state of the security provider categories represented by the specified <a href="https://msdn.microsoft.com/b32664f4-9a1d-4fd2-ab2b-e3c5a8ddf187">WSC_SECURITY_PROVIDER</a> enumeration values.


## -parameters




### -param Providers [in]

One or more of the values in the <a href="https://msdn.microsoft.com/b32664f4-9a1d-4fd2-ab2b-e3c5a8ddf187">WSC_SECURITY_PROVIDER</a> enumeration. To specify more than one value, combine the individual values by performing a bitwise OR operation.


### -param pHealth [out]

A pointer to a variable that takes the value of one of the members of the <a href="https://msdn.microsoft.com/a5f34088-13b9-4269-a3ca-777e0bb9b655">WSC_SECURITY_PROVIDER_HEALTH</a> enumeration. If more than one provider is specified in the <i>Providers</i> parameter, the value of this parameter is the health of the least healthy of the specified provider categories.


## -returns



Returns <b>S_OK</b> if the function succeeds, otherwise returns an error code. If the WSC service is not running, the return value is always <b>S_FALSE</b> and the <i>pHealth</i> out parameter is always set to <b>WSC_SECURITY_PROVIDER_HEALTH_POOR</b>.




## -see-also




<a href="https://msdn.microsoft.com/a5f34088-13b9-4269-a3ca-777e0bb9b655">WSC_SECURITY_PROVIDER_HEALTH</a>
 

 


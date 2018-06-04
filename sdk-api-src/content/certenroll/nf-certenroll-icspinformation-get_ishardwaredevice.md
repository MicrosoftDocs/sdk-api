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

# ICspInformation::get_IsHardwareDevice


## -description


The <b>IsHardwareDevice</b> property retrieves a Boolean value that determines whether the provider is implemented in a hardware device.

This property is read-only.


## -parameters


## -remarks



This property only specifies whether a provider is implemented in hardware. Because a provider can be implemented in both hardware and software, you cannot assume that a value of true for this property  indicates that there is no software component. You must also examine the <a href="https://msdn.microsoft.com/50f78dcc-4d32-40c9-8153-f0b6ac72c03b">IsSoftwareDevice</a> property. The following providers return true for the <b>IsHardwareDevice</b> property:<ul>
<li>Microsoft Smart Card Key Storage Provider</li>
<li>Microsoft Base Smart Card Crypto Provider</li>
</ul>


Both of these providers also return true for the <a href="https://msdn.microsoft.com/50f78dcc-4d32-40c9-8153-f0b6ac72c03b">IsSoftwareDevice</a> property. The Certificate Enrollment service assumes that a provider is a smart card provider if both the <b>IsHardwareDevice</b> and <b>IsSoftwareDevice</b> properties are set, or if the <a href="https://msdn.microsoft.com/ee67670b-80a9-4637-a5ed-84d3430853ea">IsRemovable</a> property is set.




## -see-also




<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>
 

 


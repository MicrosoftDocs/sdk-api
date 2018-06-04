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

# ICspInformation::get_IsRemovable


## -description


The <b>IsRemovable</b> property retrieves a Boolean value that specifies whether the token that contains the key can be removed.

This property is read-only.


## -parameters


## -remarks



Operator cards and  smart cards are examples of removable tokens that can contain keys. For example, the following providers return true for this property value:<ul>
<li>Microsoft Smart Card Key Storage Provider</li>
<li>Microsoft Base Smart Card Crypto Provider</li>
</ul>


The Certificate Enrollment service assumes that a provider is a smart card provider if both the <a href="https://msdn.microsoft.com/d69ade8c-3b74-4391-9048-6511f3d7e9fa">IsHardwareDevice</a> and <a href="https://msdn.microsoft.com/50f78dcc-4d32-40c9-8153-f0b6ac72c03b">IsSoftwareDevice</a> properties are set, or if the <b>IsRemovable</b> property is set.




## -see-also




<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>
 

 


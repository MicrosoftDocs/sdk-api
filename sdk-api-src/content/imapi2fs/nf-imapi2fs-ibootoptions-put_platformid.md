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

# IBootOptions::put_PlatformId


## -description


Sets the platform identifier that identifies the operating system architecture that the boot image supports.


## -parameters




### -param newVal [in]

Identifies the operating system architecture that the boot image supports. For possible values, see the <a href="https://msdn.microsoft.com/296f9da1-99be-4d20-8961-f99cf220404a">PlatformId</a> enumeration type. The default value is  <b>PlatformX86</b> for Intel x86–based platforms.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -see-also




<a href="https://msdn.microsoft.com/446b535c-d576-4f96-8b74-305e34cb99d4">IBootOptions</a>



<a href="https://msdn.microsoft.com/8d5ceb0e-4fd2-4146-8e15-b157c80a9d5b">IBootOptions::get_PlatformId</a>
 

 


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

# IdentityType enumeration


## -description


Represents the kind of activation for an out-of-process server.


## -enum-fields




### -field IdentityType_ActivateAsActivator


### -field IdentityType_RunAs


### -field IdentityType_ActivateAsPackage


### -field IdentityType_SessionVirtual


### -field IdentityType_SessionUser


### -field IdentityType_ActivateAsActivatingUser


### -field int




#### - ActivateAsActivator

Activate the out-of-process server as an activator.


#### - ActivateAsPackage

Activate the out-of-process server as a Windows Store app package.


#### - RunAs

Activate the out-of-process server as an executable.


## -see-also




<a href="https://msdn.microsoft.com/1D8F7B12-2883-478D-B83D-84AC47D512E4">IExeServerActivatableClassRegistration</a>



<a href="https://msdn.microsoft.com/9A96968D-B9BD-4C47-B626-69B6EA6AE7EA">IExeServerRegistration</a>
 

 


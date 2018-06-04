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

# _SP_REMOVEDEVICE_PARAMS structure


## -description


An SP_REMOVEDEVICE_PARAMS structure corresponds to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff543717">DIF_REMOVE</a> installation request.


## -struct-fields




### -field ClassInstallHeader

An install request header that contains the header size and the DIF code for the request. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552340">SP_CLASSINSTALL_HEADER</a>. 


### -field Scope

Flags that indicate the scope of the device removal. Can be one of the following values:





#### DI_REMOVEDEVICE_GLOBAL

Make this change in all hardware profiles. Remove information about the device from the registry.



#### DI_REMOVEDEVICE_CONFIGSPECIFIC

Make this change to only the hardware profile specified by <b>HwProfile</b>. this flag only applies to root-enumerated devices. When Windows removes the device from the last hardware profile in which it was configured, Windows performs a global removal.


### -field HwProfile

The hardware profile ID for profile-specific changes. Zero specifies the current hardware profile. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543717">DIF_REMOVE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552340">SP_CLASSINSTALL_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550922">SetupDiCallClassInstaller</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552097">SetupDiRemoveDevice</a>
 

 


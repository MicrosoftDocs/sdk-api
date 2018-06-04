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

# _SP_PROPCHANGE_PARAMS structure


## -description


An SP_PROPCHANGE_PARAMS structure corresponds to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff543712">DIF_PROPERTYCHANGE</a> installation request.


## -struct-fields




### -field ClassInstallHeader

An install request header that contains the header size and the DIF code for the request. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552340">SP_CLASSINSTALL_HEADER</a>. 


### -field StateChange

State change action. Can be one of the following values:





#### DICS_ENABLE

The device is being enabled.

For this state change, Windows enables the device if the <b>DICS_FLAG_GLOBAL</b> flag is specified. 

If the <b>DICS_FLAG_CONFIGSPECIFIC</b> flag is specified and the current hardware profile is specified then Windows enables the device. If the <b>DICS_FLAG_CONFIGSPECIFIC</b> is specified and not the current hardware profile then Windows sets some flags in the registry and does not change the device's state. Windows will change the device state when the specified profile becomes the current profile.



#### DICS_DISABLE

The device is being disabled.

For this state change, Windows disables the device if the <b>DICS_FLAG_GLOBAL</b> flag is specified. 

If the <b>DICS_FLAG_CONFIGSPECIFIC</b> flag is specified and the current hardware profile is specified then Windows disables the device. If the <b>DICS_FLAG_CONFIGSPECIFIC</b> is specified and not the current hardware profile then Windows sets some flags in the registry and does not change the device's state. 



#### DICS_PROPCHANGE

The properties of the device have changed. 

For this state change, Windows ignores the <b>Scope</b> information as long it is a valid value, and stops and restarts the device.



#### DICS_START

The device is being started (if the request is for the currently active hardware profile). 

<b>DICS_START</b> must be <b>DICS_FLAG_CONFIGSPECIFIC</b>. You cannot perform that change globally. 

Windows only starts the device if the current hardware profile is specified. Otherwise, Windows sets a registry flag and does not change the state of the device.



#### DICS_STOP

The device is being stopped. The driver stack will be unloaded and the CSCONFIGFLAG_DO_NOT_START flag will be set for the device.

<b>DICS_STOP</b> must be <b>DICS_FLAG_CONFIGSPECIFIC</b>. You cannot perform that change globally. 

Windows only stops the device if the current hardware profile is specified. Otherwise, Windows sets a registry flag and does not change the state of the device.

Components should not specify DICS_STOP or DICS_START. Instead, they should use DICS_PROPCHANGE to stop and restart a device to cause changes in the device's configuration to take effect.


### -field Scope

Flags that specify the scope of a device property change. Can be one of the following:





#### DICS_FLAG_GLOBAL

Make the change in all hardware profiles.



#### DICS_FLAG_CONFIGSPECIFIC

Make the change in the specified profile only.

The following flag is obsolete:





#### DICS_FLAG_CONFIGGENERAL


### -field HwProfile

Supplies the hardware profile ID for profile-specific changes. Zero specifies the current hardware profile.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543712">DIF_PROPERTYCHANGE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552340">SP_CLASSINSTALL_HEADER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550922">SetupDiCallClassInstaller</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550930">SetupDiChangeState</a>
 

 


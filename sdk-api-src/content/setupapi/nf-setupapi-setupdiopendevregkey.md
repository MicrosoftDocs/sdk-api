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

# SetupDiOpenDevRegKey function


## -description


The <b>SetupDiOpenDevRegKey</b> function opens a registry key for device-specific configuration information.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> that contains a device information element that represents the device for which to open a registry key.


### -param DeviceInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.


### -param Scope [in]

The scope of the registry key to open. The scope determines where the information is stored. The scope can be global or specific to a hardware profile. The scope is specified by one of the following values:





#### DICS_FLAG_GLOBAL

Open a key to store global configuration information. This information is not specific to a particular hardware profile. This opens a key that is rooted at <b>HKEY_LOCAL_MACHINE.</b> The exact key opened depends on the value of the <i>KeyType</i> parameter.



#### DICS_FLAG_CONFIGSPECIFIC

Open a key to store hardware profile-specific configuration information. This key is rooted at one of the hardware-profile specific branches, instead of <b>HKEY_LOCAL_MACHINE</b>. The exact key opened depends on the value of the <i>KeyType</i> parameter.


### -param HwProfile [in]

A hardware profile value, which is set as follows:

<ul>
<li>
If <i>Scope</i> is set to DICS_FLAG_CONFIGSPECIFIC, <i>HwProfile</i> specifies the hardware profile of the key that is to be opened. 

</li>
<li>
If <i>HwProfile</i> is 0, the key for the current hardware profile is opened. 

</li>
<li>
If <i>Scope</i> is DICS_FLAG_GLOBAL, <i>HwProfile</i> is ignored.

</li>
</ul>

### -param KeyType [in]

The type of registry storage key to open, which can be one of the following values:





#### DIREG_DEV

Open a <a href="https://msdn.microsoft.com/3be5c842-d1b6-4c34-8990-e23e2d08dd23">hardware key</a> for the device. 



#### DIREG_DRV

Open a <a href="https://msdn.microsoft.com/5f6fec1a-1134-4765-81be-9b50939e5e66">software key</a> for the device. 

For more information about a device's hardware and software keys, see <a href="devinst.registry_trees_and_keys">Registry Trees and Keys for Devices and Drivers</a>.


### -param samDesired [in]

The registry security access that is required for the requested key. For information about registry security access values of type REGSAM, see the Microsoft Windows SDK documentation. 


## -returns



If the function is successful, it returns a handle to an opened registry key where private configuration data about this device instance can be stored/retrieved.

If the function fails, it returns INVALID_HANDLE_VALUE. To get extended error information, call <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



Depending on the value that is passed in the <i>samDesired</i> parameter, it might be necessary for the caller of this function to be a member of the Administrators group.

Close the handle returned from this function by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=194543">RegCloseKey</a>.

The specified device instance must be registered before this function is called. However, be aware that the operating system automatically registers PnP device instances. For information about how to register non-PnP device instances, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff552091">SetupDiRegisterDeviceInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550973">SetupDiCreateDevRegKey</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550952">SetupDiCreateDeviceInfo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551997">SetupDiGetHwProfileList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552091">SetupDiRegisterDeviceInfo</a>
 

 


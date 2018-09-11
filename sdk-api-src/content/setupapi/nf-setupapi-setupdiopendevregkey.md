---
UID: NF:setupapi.SetupDiOpenDevRegKey
title: SetupDiOpenDevRegKey function
author: windows-sdk-content
description: The SetupDiOpenDevRegKey function opens a registry key for device-specific configuration information.
old-location: devinst\setupdiopendevregkey.htm
tech.root: devinst
ms.assetid: ffa435c8-4a73-454e-be36-cd90ba6e6d11
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: SetupDiOpenDevRegKey, SetupDiOpenDevRegKey function [Device and Driver Installation], devinst.setupdiopendevregkey, di-rtns_074a28c6-e847-439c-a694-36a196e418b6.xml, setupapi/SetupDiOpenDevRegKey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: DesktopFor universal, call CM_Open_DevNode_Key
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupDiOpenDevRegKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiOpenDevRegKey function


## -description


The <b>SetupDiOpenDevRegKey</b> function opens a registry key for device-specific configuration information.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="https://msdn.microsoft.com/library/Ff541247(v=VS.85).aspx">device information set</a> that contains a device information element that represents the device for which to open a registry key.


### -param DeviceInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.


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

For more information about a device's hardware and software keys, see <a href="https://msdn.microsoft.com/library/Ff549815(v=VS.85).aspx">Registry Trees and Keys for Devices and Drivers</a>.


### -param samDesired [in]

The registry security access that is required for the requested key. For information about registry security access values of type REGSAM, see the Microsoft Windows SDK documentation. 


## -returns



If the function is successful, it returns a handle to an opened registry key where private configuration data about this device instance can be stored/retrieved.

If the function fails, it returns INVALID_HANDLE_VALUE. To get extended error information, call <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



Depending on the value that is passed in the <i>samDesired</i> parameter, it might be necessary for the caller of this function to be a member of the Administrators group.

Close the handle returned from this function by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=194543">RegCloseKey</a>.

The specified device instance must be registered before this function is called. However, be aware that the operating system automatically registers PnP device instances. For information about how to register non-PnP device instances, see <a href="https://msdn.microsoft.com/76b2d1ab-3efb-46e6-8c44-d6913b0eecd5">SetupDiRegisterDeviceInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/8c07db95-eb59-4e01-851d-f6a8da169625">SetupDiCreateDevRegKey</a>



<a href="https://msdn.microsoft.com/7d42167f-9af4-4aee-b641-a93ade1e3969">SetupDiCreateDeviceInfo</a>



<a href="https://msdn.microsoft.com/59fc7202-0e03-4eaa-b3ca-7d55be767b1a">SetupDiGetHwProfileList</a>



<a href="https://msdn.microsoft.com/76b2d1ab-3efb-46e6-8c44-d6913b0eecd5">SetupDiRegisterDeviceInfo</a>
 

 


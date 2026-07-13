---
UID: NF:setupapi.SetupDiOpenDevRegKey
title: SetupDiOpenDevRegKey function (setupapi.h)
description: The SetupDiOpenDevRegKey function opens a registry key for device-specific configuration information.
helpviewer_keywords: ["SetupDiOpenDevRegKey","SetupDiOpenDevRegKey function [Device and Driver Installation]","devinst.setupdiopendevregkey","di-rtns_074a28c6-e847-439c-a694-36a196e418b6.xml","setupapi/SetupDiOpenDevRegKey"]
old-location: devinst\setupdiopendevregkey.htm
tech.root: devinst
ms.assetid: ffa435c8-4a73-454e-be36-cd90ba6e6d11
ms.date: 12/05/2018
ms.keywords: SetupDiOpenDevRegKey, SetupDiOpenDevRegKey function [Device and Driver Installation], devinst.setupdiopendevregkey, di-rtns_074a28c6-e847-439c-a694-36a196e418b6.xml, setupapi/SetupDiOpenDevRegKey
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiOpenDevRegKey
 - setupapi/SetupDiOpenDevRegKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-setupapi-devobj-l1-1-0.dll
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupDiOpenDevRegKey
req.apiset: ext-ms-win-setupapi-classinstallers-l1-1-2 (introduced in Windows 10, version 10.0.14393)
---

# SetupDiOpenDevRegKey function


## -description

The <b>SetupDiOpenDevRegKey</b> function opens a registry key for device-specific configuration information.

## -parameters

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains a device information element that represents the device for which to open a registry key.

### -param DeviceInfoData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.

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

Open a <a href="/windows-hardware/drivers/">hardware key</a> for the device. 



#### DIREG_DRV

Open a <a href="/windows-hardware/drivers/">software key</a> for the device. 

For more information about a device's hardware and software keys, see <a href="/windows-hardware/drivers/install/registry-trees-and-keys">Registry Trees and Keys for Devices and Drivers</a>.

### -param samDesired [in]

The registry security access that is required for the requested key. For information about registry security access values of type REGSAM, see the Microsoft Windows SDK documentation.

## -returns

If the function is successful, it returns a handle to an opened registry key where private configuration data about this device instance can be stored/retrieved.

If the function fails, it returns INVALID_HANDLE_VALUE. To get extended error information, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Depending on the value that is passed in the <i>samDesired</i> parameter, it might be necessary for the caller of this function to be a member of the Administrators group.

Close the handle returned from this function by calling <a href="/windows/win32/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>.

The specified device instance must be registered before this function is called. However, be aware that the operating system automatically registers PnP device instances. For information about how to register non-PnP device instances, see <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiregisterdeviceinfo">SetupDiRegisterDeviceInfo</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedevregkeya">SetupDiCreateDevRegKey</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinfoa">SetupDiCreateDeviceInfo</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigethwprofilelist">SetupDiGetHwProfileList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiregisterdeviceinfo">SetupDiRegisterDeviceInfo</a>

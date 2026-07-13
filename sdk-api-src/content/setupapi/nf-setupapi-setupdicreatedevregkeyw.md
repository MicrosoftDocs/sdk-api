---
UID: NF:setupapi.SetupDiCreateDevRegKeyW
title: SetupDiCreateDevRegKeyW function (setupapi.h)
description: The SetupDiCreateDevRegKey function creates a registry key for device-specific configuration information and returns a handle to the key. (Unicode)
helpviewer_keywords: ["SetupDiCreateDevRegKey", "SetupDiCreateDevRegKey function [Device and Driver Installation]", "SetupDiCreateDevRegKeyW", "devinst.setupdicreatedevregkey", "di-rtns_284367d1-6053-4fd1-990b-7028a116ece2.xml", "setupapi/SetupDiCreateDevRegKey"]
old-location: devinst\setupdicreatedevregkey.htm
tech.root: devinst
ms.assetid: 8c07db95-eb59-4e01-851d-f6a8da169625
ms.date: 12/05/2018
ms.keywords: SetupDiCreateDevRegKey, SetupDiCreateDevRegKey function [Device and Driver Installation], SetupDiCreateDevRegKeyA, SetupDiCreateDevRegKeyW, devinst.setupdicreatedevregkey, di-rtns_284367d1-6053-4fd1-990b-7028a116ece2.xml, setupapi/SetupDiCreateDevRegKey
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiCreateDevRegKeyW
 - setupapi/SetupDiCreateDevRegKeyW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - ext-ms-win-setupapi-devobj-l1-1-0.dll
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiCreateDevRegKey - SetupDiCreateDevRegKeyW
---

# SetupDiCreateDevRegKeyW function


## -description

The <b>SetupDiCreateDevRegKey</b> function creates a registry key for device-specific configuration information and returns a handle to the key.

## -parameters

### -param DeviceInfoSet [in]

A handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains a device information element that represents the device for which to create a registry key.

### -param DeviceInfoData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.

### -param Scope [in]

The scope of the registry key to be created. The scope determines where the information is stored. The key created can be global or hardware profile-specific. Can be one of the following values:





#### DICS_FLAG_GLOBAL

Create a key to store global configuration information. This information is not specific to a particular hardware profile. On NT-based operating systems this creates a key that is rooted at <b>HKEY_LOCAL_MACHINE</b>. The exact key opened depends on the value of the <i>KeyType</i> parameter.



#### DICS_FLAG_CONFIGSPECIFIC

Create a key to store hardware profile-specific configuration information. This key is rooted at one of the hardware-profile specific branches, instead of <b>HKEY_LOCAL_MACHINE</b>.

### -param HwProfile [in]

The hardware profile for which to create a key if <i>HwProfileFlags</i> is set to SPDICS_FLAG_CONFIGSPECIFIC. If <i>HwProfile</i> is 0, the key for the current hardware profile is created. If <i>HwProfileFlags</i> is SPDICS_FLAG_GLOBAL, <i>HwProfile</i> is ignored.

### -param KeyType [in]

The type of registry storage key to create. Can be one of the following values:





#### DIREG_DEV

Create a <a href="/windows-hardware/drivers/">hardware key</a> for the device. 



#### DIREG_DRV

Create a <a href="/windows-hardware/drivers/">software key</a> for the device.

### -param InfHandle [in, optional]

The handle to an open INF file that contains an <a href="/windows-hardware/drivers/install/inf-ddinstall-section">INF DDInstall section</a> to be executed for the newly created key. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <i>InfSectionName</i> must be specified as well.

### -param InfSectionName [in, optional]

The name of an INF <i>DDInstall</i> section in the INF file specified by <i>InfHandle</i>. This section is executed for the newly created key. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <i>InfHandle</i> must be specified as well.


##### - KeyType.DIREG_DEV

Create a <a href="/windows-hardware/drivers/">hardware key</a> for the device. 


##### - KeyType.DIREG_DRV

Create a <a href="/windows-hardware/drivers/">software key</a> for the device.


##### - Scope.DICS_FLAG_CONFIGSPECIFIC

Create a key to store hardware profile-specific configuration information. This key is rooted at one of the hardware-profile specific branches, instead of <b>HKEY_LOCAL_MACHINE</b>.


##### - Scope.DICS_FLAG_GLOBAL

Create a key to store global configuration information. This information is not specific to a particular hardware profile. On NT-based operating systems this creates a key that is rooted at <b>HKEY_LOCAL_MACHINE</b>. The exact key opened depends on the value of the <i>KeyType</i> parameter.

## -returns

If <b>SetupDiCreateDevRegKey</b> succeeds, the function returns a handle to the specified registry key in which device-specific configuration data can be stored and retrieved. If <b>SetupDiCreateDevRegKey</b> fails, the function returns INVALID_HANDLE_VALUE. Call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to get extended error information.

## -remarks

The caller of <b>SetupDiCreateDevRegKey</b> must be a member of the Administrators group.

Close the handle returned from <b>SetupDiCreateDevRegKey</b> by calling <a href="/windows/win32/api/winreg/nf-winreg-regclosekey">RegCloseKey</a>.

If the specified key already exists, <b>SetupDiCreateDevRegKey</b> returns a handle to that key. Otherwise, <b>SetupDiCreateDevRegKey</b> creates the specified key and returns a handle to the new key. For Windows Server 2003 and later versions of Windows, the key handle has KEY_READ and KEY_WRITE access only. For previous Windows versions, this handle has KEY_ALL_ACCESS access. 

The specified device instance must be registered before <b>SetupDiCreateDevRegKey</b> is called. Note, however, that the operating system automatically registers PnP device instances. For information about how to register non-PnP device instances, see <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiregisterdeviceinfo">SetupDiRegisterDeviceInfo</a>.

For installations that use layout files (specified by the <b>LayoutFile</b> entry in an <a href="/windows-hardware/drivers/install/inf-version-section">INF Version section</a>), the layout file must be opened by a call to <b>SetupOpenAppendInfFile</b> (described in the Microsoft Windows SDK documentation) before <b>SetupDiCreateDevRegKey</b> is called.

If the supplied device information set contains device information elements for a remote system, and <i>InfHandle</i> and <i>InfSectionName</i> are also specified, the create request will fail, and a subsequent call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return ERROR_REMOTE_REQUEST_UNSUPPORTED.





> [!NOTE]
> The setupapi.h header defines SetupDiCreateDevRegKey as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinfoa">SetupDiCreateDeviceInfo</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigethwprofilelist">SetupDiGetHwProfileList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopendevregkey">SetupDiOpenDevRegKey</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiregisterdeviceinfo">SetupDiRegisterDeviceInfo</a>

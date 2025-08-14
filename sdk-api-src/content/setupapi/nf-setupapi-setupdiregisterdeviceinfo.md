---
UID: NF:setupapi.SetupDiRegisterDeviceInfo
title: SetupDiRegisterDeviceInfo function (setupapi.h)
description: The SetupDiRegisterDeviceInfo function is the default handler for the DIF_REGISTERDEVICE request.
helpviewer_keywords: ["SetupDiRegisterDeviceInfo","SetupDiRegisterDeviceInfo function [Device and Driver Installation]","devinst.setupdiregisterdeviceinfo","di-rtns_ab9a56a2-3256-472f-a818-32918efd5673.xml","setupapi/SetupDiRegisterDeviceInfo"]
old-location: devinst\setupdiregisterdeviceinfo.htm
tech.root: devinst
ms.assetid: 76b2d1ab-3efb-46e6-8c44-d6913b0eecd5
ms.date: 12/05/2018
ms.keywords: SetupDiRegisterDeviceInfo, SetupDiRegisterDeviceInfo function [Device and Driver Installation], devinst.setupdiregisterdeviceinfo, di-rtns_ab9a56a2-3256-472f-a818-32918efd5673.xml, setupapi/SetupDiRegisterDeviceInfo
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
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiRegisterDeviceInfo
 - setupapi/SetupDiRegisterDeviceInfo
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
api_name:
 - SetupDiRegisterDeviceInfo
---

# SetupDiRegisterDeviceInfo function


## -description

The 
   <b>SetupDiRegisterDeviceInfo</b> function is the default handler for the <a href="/windows-hardware/drivers/install/dif-registerdevice">DIF_REGISTERDEVICE</a> request.

## -parameters

### -param DeviceInfoSet [in]

A handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains a device information element that represents the device to register. The device information set must not contain any remote elements.

### -param DeviceInfoData [in, out]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. This is an IN-OUT parameter because <i>DeviceInfoData.</i><b>DevInst</b> might be updated with a new handle value upon return.

### -param Flags [in]

A flag value that controls how the device is registered, which can be zero or the following value:





#### SPRDI_FIND_DUPS

Search for a previously-existing <a href="/windows-hardware/drivers/">device instance</a> that corresponds to the device that is represented by <i>DeviceInfoData</i>. If this flag is not specified, the device instance is registered regardless of whether a device instance already exists for it.

If the caller supplies <i>CompareProc</i>, the caller must also set this flag.

### -param CompareProc [in, optional]

A pointer to a comparison callback function to use in duplicate detection. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, the callback function is called for each device instance that is of the same class as the device instance that is being registered. The prototype of the callback function is as follows:


```
typedef  DWORD (CALLBACK* PSP_DETSIG_CMPPROC) (
    IN HDEVINFO  DeviceInfoSet,
    IN PSP_DEVINFO_DATA  NewDeviceData,
    IN PSP_DEVINFO_DATA  ExistingDeviceData,
    IN PVOID  CompareContextOPTIONAL
    );
```


The compare function must return ERROR_DUPLICATE_FOUND if it finds that the two devices are duplicates. Otherwise, it should return NO_ERROR. If some other error is encountered, the callback function should return the appropriate ERROR_* code to indicate the failure.

If <i>CompareProc</i> is not specified and duplication detection is requested, a default comparison behavior is used. The default is to compare the new device's detect signature with the detect signature of all other devices in the class. The detect signature is contained in the class-specific resource descriptor of the device's boot log configuration.

### -param CompareContext [in, optional]

A pointer to a caller-supplied context buffer that is passed into the callback function. This parameter is ignored if <i>CompareProc</i> is not specified.

### -param DupDeviceInfoData [out, optional]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure to receive information about a duplicate device instance, if any, discovered as a result of attempting to register this device. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, the caller must set <i>DupDeviceInfoData.</i><b>cbSize</b> to <b>sizeof</b>(SP_DEVINFO_DATA). This will be filled in if the function returns <b>FALSE</b>, and <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_DUPLICATE_FOUND. This device information element is added as a member of the specified <i>DeviceInfoSet</i>, if not already a member. If <i>DupDeviceInfoData</i> is not specified, the duplicate is not added to the device information set.

If you call this function when handling a <a href="/windows-hardware/drivers/install/dif-registerdevice">DIF_REGISTERDEVICE</a> request, the <i>DupDeviceInfoData</i> parameter must be <b>NULL</b>.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>SetupDiRegisterDeviceInfo</b> is primarily designed to register a non-PnP device with the <a href="/windows-hardware/drivers/install/pnp-manager">Plug and Play (PnP) manager</a> on a local computer. Although <b>SetupDiRegisterDeviceInfo</b> will not fail if the device information set is for a remote computer, the result is of limited use because the device information set cannot subsequently be used with DIF_<i>Xxx</i> installation requests or <b>SetupDi</b><i>Xxx</i> functions that do not support operations on a remote computer. For example, calling <b>SetupDiCreateDevRegKey</b> to execute an INF section for a newly registered device on a remote computer will fail.

<div class="alert"><b>Note</b>  Only a class installer should call <b>SetupDiRegisterDeviceInfo</b> and only in those situations where the class installer must perform device registration operations after <b>SetupDiRegisterDeviceInfo</b> completes the default device registration operation. In such situations, the class installer must directly call <b>SetupDiRegisterDeviceInfo</b> when the installer processes a DIF_REGISTERDEVICE request. For more information about calling the default handler, see <a href="/windows-hardware/drivers/install/calling-the-default-dif-code-handlers">Calling Default DIF Code Handlers</a>.</div>
<div> </div>
After registering a device information element, the caller should update any stored copies of the <b>DevInst</b> handle associated with this device. This is necessary because the handle value might have changed during registration. The caller does not have to retrieve the SP_DEVINFO_DATA structure again because the <b>DevInst</b> field of the structure is updated to reflect the current value of the handle. 

Do not directly call this function for PnP device instances. PnP device instances are automatically registered by the operating system. However, you must register non-PnP device instances in one of the following ways:

<ol>
<li>
If your installation application uses a <a href="/windows-hardware/drivers/install/dif-detect">DIF_DETECT</a> request to successfully detect a device, it should also use a DIF_REGISTERDEVICE request to register the device instance. The request should be handled in the default manner. (By default, <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a> first calls the class installer and class co-installers to do duplicate detection and register the device instance. If these installers do not register the device instance, <b>SetupDiCallClassInstaller</b> calls <b>SetupDiRegisterDeviceInfo</b> to do duplicate detection and register the device instance.)

</li>
<li>
If your installation application creates a device instance (for example, by calling <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinfoa">SetupDiCreateDeviceInfo</a>) but does not do duplicate detection, your installation application should use a DIF_REGISTERDEVICE request to register the device instance. The request should be handled in the default manner as described earlier.

</li>
<li>
If your installation application creates a new device and does duplicate detection, your installation application should use a DIF_REGISTERDEVICE request but should prevent <b>SetupDiCallClassInstaller</b> from calling <b>SetupDiRegisterDeviceInfo</b>. To prevent <b>SetupDiCallClassInstaller</b> from calling <b>SetupDiRegisterDeviceInfo</b>, set the DI_NODI_DEFAULTACTION flag in the <b>Flags</b> member of the SP_DEVINSTALL_PARAMS structure for the device instance.

If <b>SetupDiCallClassInstaller</b> returns <b>TRUE</b> for the DIF_REGISTERDEVICE request, the class installer or class co-installers registered the device instance. In this case, the installation application can continue to install the device.

If <b>SetupDiCallClassInstaller</b> returns <b>FALSE</b> for the DIF_REGISTERDEVICE request, the class installer or class co-installers did not register the device instance. In this case, the installation application should do one of the following, depending on the last error that <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns for the request:

<ul>
<li>If the last error is ERROR_DI_DO_DEFAULT, the installation application can directly call <b>SetupDiRegisterDeviceInfo</b> and supply a <i>CompareProc</i> to do duplicate detection. If this call is successful and no duplicates are found, device installation can continue. If a duplicate is found, <b>SetupDiRegisterDeviceInfo</b> returns <b>FALSE</b>, and the installation application must terminate device installation.</li>
<li>If the last error is not ERROR_DI_DO_DEFAULT, the installation application must terminate device installation.</li>
</ul>
The caller of <b>SetupDiRegisterDeviceInfo</b> must be a member of the Administrators group.

</li>
</ol>

## -see-also

<a href="/windows-hardware/drivers/install/dif-registerdevice">DIF_REGISTERDEVICE</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinstall_params_a">SP_DEVINSTALL_PARAMS</a>
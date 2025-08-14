---
UID: NF:setupapi.SetupDiEnumDeviceInterfaces
title: SetupDiEnumDeviceInterfaces function (setupapi.h)
description: The SetupDiEnumDeviceInterfaces function enumerates the device interfaces that are contained in a device information set.
helpviewer_keywords: ["SetupDiEnumDeviceInterfaces","SetupDiEnumDeviceInterfaces function [Device and Driver Installation]","devinst.setupdienumdeviceinterfaces","di-rtns_1fd59eb7-0934-4747-9a0e-81dac96c23ef.xml","setupapi/SetupDiEnumDeviceInterfaces"]
old-location: devinst\setupdienumdeviceinterfaces.htm
tech.root: devinst
ms.assetid: 5095404d-2447-407e-99e2-dd3ef3c3b905
ms.date: 12/05/2018
ms.keywords: SetupDiEnumDeviceInterfaces, SetupDiEnumDeviceInterfaces function [Device and Driver Installation], devinst.setupdienumdeviceinterfaces, di-rtns_1fd59eb7-0934-4747-9a0e-81dac96c23ef.xml, setupapi/SetupDiEnumDeviceInterfaces
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
 - SetupDiEnumDeviceInterfaces
 - setupapi/SetupDiEnumDeviceInterfaces
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
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-1.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupDiEnumDeviceInterfaces
req.apiset: ext-ms-win-setupapi-classinstallers-l1-1-2 (introduced in Windows 10, version 10.0.14393)
---

# SetupDiEnumDeviceInterfaces function


## -description

The <b>SetupDiEnumDeviceInterfaces</b> function enumerates the device interfaces that are contained in a device information set.

## -parameters

### -param DeviceInfoSet [in]

A pointer to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains the device interfaces for which to return information. This handle is typically returned by <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevs</a>.

### -param DeviceInfoData [in, optional]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies a device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiEnumDeviceInterfaces</b> constrains the enumeration to the interfaces that are supported by the specified device. If this parameter is <b>NULL</b>, repeated calls to <b>SetupDiEnumDeviceInterfaces</b> return information about the interfaces that are associated with all the device information elements in <i>DeviceInfoSet</i>. This pointer is typically returned by <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinfo">SetupDiEnumDeviceInfo</a>.

### -param InterfaceClassGuid [in]

A pointer to a GUID that specifies the device interface class for the requested interface.

### -param MemberIndex [in]

A zero-based index into the list of interfaces in the device information set. The caller should call this function first with <i>MemberIndex</i> set to zero to obtain the first interface. Then, repeatedly increment <i>MemberIndex</i> and retrieve an interface until this function fails and <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_NO_MORE_ITEMS.

If <i>DeviceInfoData</i> specifies a particular device, the <i>MemberIndex</i> is relative to only the interfaces exposed by that device.

### -param DeviceInterfaceData [out]

A pointer to a caller-allocated buffer that contains, on successful return, a completed <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_device_interface_data">SP_DEVICE_INTERFACE_DATA</a> structure that identifies an interface that meets the search parameters. The caller must set <i>DeviceInterfaceData</i>.<b>cbSize</b> to <b>sizeof</b>(SP_DEVICE_INTERFACE_DATA) before calling this function.

## -returns

<b>SetupDiEnumDeviceInterfaces</b> returns <b>TRUE</b> if the function completed without error. If the function completed with an error, <b>FALSE</b> is returned and the error code for the failure can be retrieved by calling <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Repeated calls to this function return an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_device_interface_data">SP_DEVICE_INTERFACE_DATA</a> structure for a different device interface. This function can be called repeatedly to get information about interfaces in a device information set that are associated with a particular device information element or that are associated with all device information elements.

<i>DeviceInterfaceData</i> points to a structure that identifies a requested device interface. To get detailed information about an interface, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinterfacedetaila">SetupDiGetDeviceInterfaceDetail</a>. The detailed information includes the name of the device interface that can be passed to a Win32 function such as <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> (described in Microsoft Windows SDK documentation) to get a handle to the interface.

See <a href="/windows-hardware/drivers/install/overview-of-device-interface-classes">Overview of Device Interface Classes</a> for more info.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinfo">SetupDiEnumDeviceInfo</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevs</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinterfacedetaila">SetupDiGetDeviceInterfaceDetail</a>

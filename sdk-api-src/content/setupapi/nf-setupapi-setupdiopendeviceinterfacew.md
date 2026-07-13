---
UID: NF:setupapi.SetupDiOpenDeviceInterfaceW
title: SetupDiOpenDeviceInterfaceW function (setupapi.h)
description: The SetupDiOpenDeviceInterface function retrieves information about a device interface and adds the interface to the specified device information set for a local system or a remote system. (Unicode)
helpviewer_keywords: ["SetupDiOpenDeviceInterface", "SetupDiOpenDeviceInterface function [Device and Driver Installation]", "SetupDiOpenDeviceInterfaceW", "devinst.setupdiopendeviceinterface", "di-rtns_4505f6a3-e634-4070-a9b3-1487c2808838.xml", "setupapi/SetupDiOpenDeviceInterface"]
old-location: devinst\setupdiopendeviceinterface.htm
tech.root: devinst
ms.assetid: 31ce43e5-08b4-4c1d-b31f-77ee4e278927
ms.date: 12/05/2018
ms.keywords: SetupDiOpenDeviceInterface, SetupDiOpenDeviceInterface function [Device and Driver Installation], SetupDiOpenDeviceInterfaceA, SetupDiOpenDeviceInterfaceW, devinst.setupdiopendeviceinterface, di-rtns_4505f6a3-e634-4070-a9b3-1487c2808838.xml, setupapi/SetupDiOpenDeviceInterface
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
 - SetupDiOpenDeviceInterfaceW
 - setupapi/SetupDiOpenDeviceInterfaceW
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
 - SetupDiOpenDeviceInterface - SetupDiOpenDeviceInterfaceW
---

# SetupDiOpenDeviceInterfaceW function


## -description

The <b>SetupDiOpenDeviceInterface</b> function retrieves information about a device interface and adds the interface to the specified device information set for a local system or a remote system.

## -parameters

### -param DeviceInfoSet [in]

A pointer to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains, or will contain, a device information element that represents the device that supports the interface to open.

### -param DevicePath [in]

A pointer to a NULL-terminated string that supplies the name of the device interface to be opened. This name is a Win32 device path that is typically received in a PnP notification structure or obtained by a previous call to <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces">SetupDiEnumDeviceInterfaces</a> and its related functions.

### -param OpenFlags [in]

Flags that determine how the device interface element is to be opened. The only valid flag is as follows: 





#### DIODI_NO_ADD

Specifies that the device information element for the underlying device will not be created if that element is not already present in the specified <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a>. For more information, see the following <b>Remarks</b> section.

### -param DeviceInterfaceData [out, optional]

A pointer to a caller-initialized  <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_device_interface_data">SP_DEVICE_INTERFACE_DATA</a> structure that receives the requested interface data. This pointer is optional and can be <b>NULL</b>. If a buffer is supplied, the caller must set the <b>cbSize</b> member of the structure to <b>sizeof(</b>SP_DEVICE_INTERFACE_DATA<b>)</b> before calling <b>SetupDiOpenDeviceInterface</b>. For more information, see the following <b>Remarks</b> section.


##### - OpenFlags.DIODI_NO_ADD

Specifies that the device information element for the underlying device will not be created if that element is not already present in the specified <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a>. For more information, see the following <b>Remarks</b> section.

## -returns

<b>SetupDiOpenDeviceInterface</b> returns <b>TRUE</b> if the function completed without error. If the function completed with an error, it returns <b>FALSE</b> and the error code for the failure can be retrieved by calling <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If a device interface element for the interface already exists in <i>DeviceInfoSet</i>, <b>SetupDiOpenDeviceInterface</b> updates the flags. Therefore, this function can be used to update the flags for a device interface. For example, an interface might have been inactive when it was first opened, but has subsequently become active. If the device information element for the underlying device is not already present in <i>DeviceInfoSet</i>, this function creates one and adds it to <i>DeviceInfoSet</i>. 

If the function successfully opens the new device interface but the caller did not supply a valid structure in the <i>DeviceInterfaceData</i> parameter, the function will return <b>FALSE</b> and a subsequent call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return ERROR_INVALID_USER_BUFFER. However, in this situation, <b>SetupDiOpenDeviceInterface</b> does add the requested interface to the device information set.

If the new device interface is successfully opened, but the caller-supplied <i>DeviceInterfaceData</i> buffer is invalid, this function returns <b>FALSE</b> and <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INVALID_USER_BUFFER. The caller's buffer error does not prevent the interface from being opened.

If the DIODI_NO_ADD flag is specified for the <i>OpenFlags</i> parameter, and a device information element for the underlying device is not already present in the specified <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a>, this function returns <b>FALSE</b> and <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_NO_SUCH_DEVICE_INTERFACE. 

When the application has finished using the information that <b>SetupDiOpenDeviceInterface</b> retrieved<b>,</b> the application must call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdideletedeviceinterfacedata">SetupDiDeleteDeviceInterfaceData</a>.


<a href="/windows/desktop/medfound/mf-devsource-attribute-source-type-vidcap-symbolic-link">MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK</a> attribute can be passed in as the value of the <i>DevicePath</i> argument of the <b>SetupDiOpenDeviceInterface</b> function.





> [!NOTE]
> The setupapi.h header defines SetupDiOpenDeviceInterface as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdideletedeviceinterfacedata">SetupDiDeleteDeviceInterfaceData</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces">SetupDiEnumDeviceInterfaces</a>

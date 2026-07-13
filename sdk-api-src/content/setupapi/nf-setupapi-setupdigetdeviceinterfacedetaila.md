---
UID: NF:setupapi.SetupDiGetDeviceInterfaceDetailA
title: SetupDiGetDeviceInterfaceDetailA function (setupapi.h)
description: The SetupDiGetDeviceInterfaceDetail function returns details about a device interface. (ANSI)
helpviewer_keywords: ["SetupDiGetDeviceInterfaceDetailA", "di-rtns_5203864c-0bc7-4a59-bdb3-ddda0dbbbf98.xml"]
old-location: devinst\setupdigetdeviceinterfacedetail.htm
tech.root: devinst
ms.assetid: fb4963f1-0ed4-483d-9f39-dcbac493bf1d
ms.date: 12/05/2018
ms.keywords: SetupDiGetDeviceInterfaceDetail, SetupDiGetDeviceInterfaceDetail function [Device and Driver Installation], SetupDiGetDeviceInterfaceDetailA, SetupDiGetDeviceInterfaceDetailW, devinst.setupdigetdeviceinterfacedetail, di-rtns_5203864c-0bc7-4a59-bdb3-ddda0dbbbf98.xml, setupapi/SetupDiGetDeviceInterfaceDetail
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
 - SetupDiGetDeviceInterfaceDetailA
 - setupapi/SetupDiGetDeviceInterfaceDetailA
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
 - SetupDiGetDeviceInterfaceDetail - SetupDiGetDeviceInterfaceDetailA
---

# SetupDiGetDeviceInterfaceDetailA function


## -description

The <b>SetupDiGetDeviceInterfaceDetail</b> function returns details about a device interface.

## -parameters

### -param DeviceInfoSet [in]

A pointer to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains the interface for which to retrieve details. This handle is typically returned by <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevs</a>.

### -param DeviceInterfaceData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_device_interface_data">SP_DEVICE_INTERFACE_DATA</a> structure that specifies the interface in <i>DeviceInfoSet</i> for which to retrieve details. A pointer of this type is typically returned by <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces">SetupDiEnumDeviceInterfaces</a>.

### -param DeviceInterfaceDetailData [out, optional]

A pointer to an <a href="/windows/win32/api/setupapi/ns-setupapi-sp_device_interface_detail_data_a">SP_DEVICE_INTERFACE_DETAIL_DATA</a> structure to receive information about the specified interface. This parameter is optional and can be <b>NULL</b>. This parameter must be <b>NULL</b> if <i>DeviceInterfaceDetailSize</i> is zero. If this parameter is specified, the caller must set <i>DeviceInterfaceDetailData</i><b>.cbSize</b> to <b>sizeof</b>(SP_DEVICE_INTERFACE_DETAIL_DATA) before calling this function. The <b>cbSize</b> member always contains the size of the fixed part of the data structure, not a size reflecting the variable-length string at the end.

### -param DeviceInterfaceDetailDataSize [in]

The size of the <i>DeviceInterfaceDetailData</i> buffer. The buffer must be at least (<b>offsetof</b>(SP_DEVICE_INTERFACE_DETAIL_DATA, <b>DevicePath</b>) + <b>sizeof</b>(TCHAR)) bytes, to contain the fixed part of the structure and a single <b>NULL</b> to terminate an empty MULTI_SZ string. 

This parameter must be zero if <i>DeviceInterfaceDetailData</i> is <b>NULL</b>.

### -param RequiredSize [out, optional]

A pointer to a variable of type DWORD that receives the required size of the <i>DeviceInterfaceDetailData</i> buffer. This size includes the size of the fixed part of the structure plus the number of bytes required for the variable-length device path string. This parameter is optional and can be <b>NULL</b>.

### -param DeviceInfoData [out, optional]

A pointer to a buffer that receives information about the device that supports the requested interface. The caller must set <i>DeviceInfoData</i><b>.cbSize</b> to <b>sizeof</b>(SP_DEVINFO_DATA). This parameter is optional and can be <b>NULL</b>.

## -returns

<b>SetupDiGetDeviceInterfaceDetail</b> returns <b>TRUE</b> if the function completed without error. If the function completed with an error, <b>FALSE</b> is returned and the error code for the failure can be retrieved by calling <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Using this function to get details about an interface is typically a two-step process:

<ol>
<li>
Get the required buffer size. Call <b>SetupDiGetDeviceInterfaceDetail</b> with a <b>NULL</b><i>DeviceInterfaceDetailData</i> pointer, a <i>DeviceInterfaceDetailDataSize</i> of zero, and a valid <i>RequiredSize</i> variable. In response to such a call, this function returns the required buffer size at <i>RequiredSize</i> and fails with <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returning ERROR_INSUFFICIENT_BUFFER.

</li>
<li>
Allocate an appropriately sized buffer and call the function again to get the interface details.

</li>
</ol>
The interface detail returned by this function consists of a device path that can be passed to Win32 functions such as <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>. Do not attempt to parse the device path symbolic name. The device path can be reused across system starts.

<b>SetupDiGetDeviceInterfaceDetail</b> can be used to get just the <i>DeviceInfoData</i>. If the interface exists but <i>DeviceInterfaceDetailData</i> is <b>NULL</b>, this function fails, <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER, and the <i>DeviceInfoData</i> structure is filled with information about the device that exposes the interface.





> [!NOTE]
> The setupapi.h header defines SetupDiGetDeviceInterfaceDetail as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces">SetupDiEnumDeviceInterfaces</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevs</a>

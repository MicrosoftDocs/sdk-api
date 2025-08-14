---
UID: NF:setupapi.SetupDiDeleteDeviceInterfaceData
title: SetupDiDeleteDeviceInterfaceData function (setupapi.h)
description: The SetupDiDeleteDeviceInterfaceData function deletes a device interface from a device information set.
helpviewer_keywords: ["SetupDiDeleteDeviceInterfaceData","SetupDiDeleteDeviceInterfaceData function [Device and Driver Installation]","devinst.setupdideletedeviceinterfacedata","di-rtns_6694af3a-5716-4ee6-b10e-2603dc341781.xml","setupapi/SetupDiDeleteDeviceInterfaceData"]
old-location: devinst\setupdideletedeviceinterfacedata.htm
tech.root: devinst
ms.assetid: 20c9fe5b-ed88-4e2c-bca5-eba62f919fe6
ms.date: 12/05/2018
ms.keywords: SetupDiDeleteDeviceInterfaceData, SetupDiDeleteDeviceInterfaceData function [Device and Driver Installation], devinst.setupdideletedeviceinterfacedata, di-rtns_6694af3a-5716-4ee6-b10e-2603dc341781.xml, setupapi/SetupDiDeleteDeviceInterfaceData
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
 - SetupDiDeleteDeviceInterfaceData
 - setupapi/SetupDiDeleteDeviceInterfaceData
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
 - SetupDiDeleteDeviceInterfaceData
---

# SetupDiDeleteDeviceInterfaceData function


## -description

The <b>SetupDiDeleteDeviceInterfaceData</b> function deletes a device interface from a device information set.

## -parameters

### -param DeviceInfoSet [in]

A pointer to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains the interface to delete. This handle is typically returned by <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevs</a>.

### -param DeviceInterfaceData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_device_interface_data">SP_DEVICE_INTERFACE_DATA</a> structure that specifies the interface in <i>DeviceInfoSet</i> to delete. This structure is typically returned by <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces">SetupDiEnumDeviceInterfaces</a>.

## -returns

<b>SetupDiDeleteDeviceInterfaceData</b> returns <b>TRUE</b> if the function completed without error. If the function completed with an error, it returns <b>FALSE</b> and the error code for the failure can be retrieved by calling <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>SetupDiDeleteDeviceInterfaceData</b> deletes a device interface element from a device information set. This function has no effect on the device interface or the underlying device.

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces">SetupDiEnumDeviceInterfaces</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevs</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea">SetupDiOpenDeviceInterface</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiremovedeviceinterface">SetupDiRemoveDeviceInterface</a>
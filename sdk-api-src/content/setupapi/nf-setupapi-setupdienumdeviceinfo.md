---
UID: NF:setupapi.SetupDiEnumDeviceInfo
title: SetupDiEnumDeviceInfo function (setupapi.h)
description: The SetupDiEnumDeviceInfo function returns a SP_DEVINFO_DATA structure that specifies a device information element in a device information set.
helpviewer_keywords: ["SetupDiEnumDeviceInfo","SetupDiEnumDeviceInfo function [Device and Driver Installation]","devinst.setupdienumdeviceinfo","di-rtns_db6730f9-381a-4da6-91b1-046fec51f270.xml","setupapi/SetupDiEnumDeviceInfo"]
old-location: devinst\setupdienumdeviceinfo.htm
tech.root: devinst
ms.assetid: 34df0557-eb86-4b00-bbd7-a4f0c1b82ff4
ms.date: 12/05/2018
ms.keywords: SetupDiEnumDeviceInfo, SetupDiEnumDeviceInfo function [Device and Driver Installation], devinst.setupdienumdeviceinfo, di-rtns_db6730f9-381a-4da6-91b1-046fec51f270.xml, setupapi/SetupDiEnumDeviceInfo
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
 - SetupDiEnumDeviceInfo
 - setupapi/SetupDiEnumDeviceInfo
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
 - Ext-MS-Win-SetupAPI-ClassInstallers-l1-1-0.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-l1-1-1.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupDiEnumDeviceInfo
req.apiset: ext-ms-win-setupapi-classinstallers-l1-1-0 (introduced in Windows 8)
---

# SetupDiEnumDeviceInfo function


## -description

The <b>SetupDiEnumDeviceInfo</b> function returns a <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies a device information element in a device information set.

## -parameters

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> for which to return an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that represents a device information element.

### -param MemberIndex [in]

A zero-based index of the device information element to retrieve.

### -param DeviceInfoData [out]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure to receive information about an enumerated device information element. The caller must set <i>DeviceInfoData</i>.<b>cbSize</b> to <code>sizeof(SP_DEVINFO_DATA)</code>.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Repeated calls to this function return a device information element for a different device. This function can be called repeatedly to get information about all devices in the device information set.

To enumerate device information elements, an installer should initially call <b>SetupDiEnumDeviceInfo</b> with the <i>MemberIndex</i> parameter set to 0. The installer should then increment <i>MemberIndex</i> and call <b>SetupDiEnumDeviceInfo</b> until there are no more values (the function fails and a call to <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_NO_MORE_ITEMS</b>).

Call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces">SetupDiEnumDeviceInterfaces</a> to get a context structure for a device <i>interface</i> element (versus a device <i>information</i> element).

An example of <b>SetupDiEnumDeviceInfo</b> usage is available on the page documenting <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevsW</a>.

## -see-also

<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicreatedeviceinfoa">SetupDiCreateDeviceInfo</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdideletedeviceinfo">SetupDiDeleteDeviceInfo</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces">SetupDiEnumDeviceInterfaces</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopendeviceinfoa">SetupDiOpenDeviceInfo</a>


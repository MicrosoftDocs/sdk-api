---
UID: NF:setupapi.SetupDiGetDeviceInstallParamsA
title: SetupDiGetDeviceInstallParamsA function (setupapi.h)

description: The SetupDiGetDeviceInstallParams function retrieves device installation parameters for a device information set or a particular device information element.
old-location: devinst\setupdigetdeviceinstallparams.htm
tech.root: devinst
ms.assetid: e5e8c203-cf71-4cb4-a7a8-5af3a2483eea

ms.date: 12/05/2018
ms.keywords: SetupDiGetDeviceInstallParams, SetupDiGetDeviceInstallParams function [Device and Driver Installation], SetupDiGetDeviceInstallParamsA, SetupDiGetDeviceInstallParamsW, devinst.setupdigetdeviceinstallparams, di-rtns_417ee0d9-f9c6-44a2-b4b4-4787fe9e952b.xml, setupapi/SetupDiGetDeviceInstallParams
ms.topic: function
f1_keywords:
- setupapi/SetupDiGetDeviceInstallParams
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- LibDef
api_location:
- Setupapi.lib
- Setupapi.dll
api_name:
- SetupDiGetDeviceInstallParams
 - SetupDiGetDeviceInstallParamsA
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupDiGetDeviceInstallParamsA function


## -description


The <b>SetupDiGetDeviceInstallParams</b> function retrieves device installation parameters for a device information set or a particular device information element.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="https://docs.microsoft.com/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains the device installation parameters to retrieve.


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiGetDeviceInstallParams</b> retrieves the installation parameters for the specified device. If this parameter is <b>NULL</b>, the function retrieves the global device installation parameters that are associated with <i>DeviceInfoSet</i>.


### -param DeviceInstallParams [out]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_devinstall_params_a">SP_DEVINSTALL_PARAMS</a> structure that receives the device install parameters. <i>DeviceInstallParams</i>.<b>cbSize</b> must be set to the size, in bytes, of the structure before calling this function.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_devinstall_params_a">SP_DEVINSTALL_PARAMS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdisetdeviceinstallparamsa">SetupDiSetDeviceInstallParams</a>
 

 


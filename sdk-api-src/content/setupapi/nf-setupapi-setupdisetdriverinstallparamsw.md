---
UID: NF:setupapi.SetupDiSetDriverInstallParamsW
title: SetupDiSetDriverInstallParamsW function (setupapi.h)

description: The SetupDiSetDriverInstallParams function sets driver installation parameters for a driver information element.
old-location: devinst\setupdisetdriverinstallparams.htm
tech.root: devinst
ms.assetid: a6084bb4-f0c1-43f3-94e7-8fd0682f5ac0

ms.date: 12/05/2018
ms.keywords: SetupDiSetDriverInstallParams, SetupDiSetDriverInstallParams function [Device and Driver Installation], SetupDiSetDriverInstallParamsA, SetupDiSetDriverInstallParamsW, devinst.setupdisetdriverinstallparams, di-rtns_31ccb1b6-757d-48d0-b3bd-1c46ac3bc4bd.xml, setupapi/SetupDiSetDriverInstallParams
ms.topic: function
f1_keywords:
- setupapi/SetupDiSetDriverInstallParams
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
- SetupDiSetDriverInstallParams
 - SetupDiSetDriverInstallParamsW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupDiSetDriverInstallParamsW function


## -description


The <b>SetupDiSetDriverInstallParams</b> function sets driver installation parameters for a driver information element.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="https://docs.microsoft.com/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains a driver information element that represents the driver for which to set installation parameters.


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies a device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be set to <b>NULL</b>. If this parameter is specified, <b>SetupDiSetDriverInstallParams</b> sets the driver installation parameters for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiSetDriverInstallParams</b> sets driver installation parameters for <i>DeviceInfoSet</i>. 


### -param DriverInfoData [in]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_drvinfo_data_v1_a">SP_DRVINFO_DATA</a> structure that specifies the driver for which installation parameters are set. If <i>DeviceInfoData</i> is specified, this driver must be a member of a driver list that is associated with <i>DeviceInfoData</i>. If <i>DeviceInfoData</i> is <b>NULL</b>, this driver must be a member of the global class driver list for <i>DeviceInfoSet</i>. 


### -param DriverInstallParams [in]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_drvinstall_params">SP_DRVINSTALL_PARAMS</a> structure that specifies the new driver install parameters. 


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupdigetdriverinstallparamsa">SetupDiGetDriverInstallParams</a>
 

 


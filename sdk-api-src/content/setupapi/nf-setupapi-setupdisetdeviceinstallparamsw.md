---
UID: NF:setupapi.SetupDiSetDeviceInstallParamsW
title: SetupDiSetDeviceInstallParamsW function
author: windows-sdk-content
description: The SetupDiSetDeviceInstallParams function sets device installation parameters for a device information set or a particular device information element.
old-location: devinst\setupdisetdeviceinstallparams.htm
old-project: devinst
ms.assetid: 20384538-e124-41f7-94a6-c0fb9f5fe6a0
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: SetupDiSetDeviceInstallParams, SetupDiSetDeviceInstallParams function [Device and Driver Installation], SetupDiSetDeviceInstallParamsA, SetupDiSetDeviceInstallParamsW, devinst.setupdisetdeviceinstallparams, di-rtns_4d977738-ea9e-4bb7-b0a6-37099647b8c8.xml, setupapi/SetupDiSetDeviceInstallParams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiSetDeviceInstallParams
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetupDiSetDeviceInstallParamsW function


## -description


The <b>SetupDiSetDeviceInstallParams</b> function sets device installation parameters for a device information set or a particular device information element.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> for which to set device installation parameters.


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies a device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be set to <b>NULL</b>. If this parameter is specified, <b>SetupDiSetDeviceInstallParams</b> sets the installation parameters for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiSetDeviceInstallParams</b> sets the installation parameters that are associated with the global class driver list for <i>DeviceInfoSet</i>.


### -param DeviceInstallParams [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552346">SP_DEVINSTALL_PARAMS</a> structure that contains the new values of the parameters. The <i>DeviceInstallParams.</i><b>cbSize</b> must be set to the size, in bytes, of the structure before this function is called.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



All parameters are validated before any changes are made. Therefore, a return value of <b>FALSE</b> indicates that no parameters were modified.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551104">SetupDiGetDeviceInstallParams</a>
 

 


---
UID: NF:setupapi.SetupDiGetDriverInstallParamsW
title: SetupDiGetDriverInstallParamsW function
author: windows-sdk-content
description: The SetupDiGetDriverInstallParams function retrieves driver installation parameters for a device information set or a particular device information element.
old-location: devinst\setupdigetdriverinstallparams.htm
old-project: devinst
ms.assetid: 7c5b0e3f-75cd-48e1-b84e-d81e4e4db7b2
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: SetupDiGetDriverInstallParams, SetupDiGetDriverInstallParams function [Device and Driver Installation], SetupDiGetDriverInstallParamsA, SetupDiGetDriverInstallParamsW, devinst.setupdigetdriverinstallparams, di-rtns_b8e7fdca-3201-42f9-86b4-a8a97be8cb90.xml, setupapi/SetupDiGetDriverInstallParams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.redist: 
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
 - SetupDiGetDriverInstallParams
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# SetupDiGetDriverInstallParamsW function


## -description


The <b>SetupDiGetDriverInstallParams</b> function retrieves driver installation parameters for a device information set or a particular device information element.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a> that contains a driver information element that represents the driver for which to retrieve installation parameters.


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that contains a device information element that represents the device for which to retrieve installation parameters. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiGetDriverInstallParams</b> retrieves information about a driver that is a member of a driver list for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiGetDriverInstallParams</b> retrieves information about a driver  that is a member of the global class driver list for <i>DeviceInfoSet</i>.


### -param DriverInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/13cdebad-6247-4651-a1d0-709e14af22f6">SP_DRVINFO_DATA</a> structure that specifies the driver information element that represents the driver for which to retrieve installation parameters. If <i>DeviceInfoData</i> is supplied, the driver must be a member of the driver list for the device that is specified by <i>DeviceInfoData</i>. Otherwise, the driver must be a member of the global class driver list for <i>DeviceInfoSet</i>.


### -param DriverInstallParams [out]

A pointer to an <a href="https://msdn.microsoft.com/300e636c-3f77-4d0b-9868-caaf92d87bfd">SP_DRVINSTALL_PARAMS</a> structure to receive the installation parameters for this driver. 


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/a6084bb4-f0c1-43f3-94e7-8fd0682f5ac0">SetupDiSetDriverInstallParams</a>
 

 


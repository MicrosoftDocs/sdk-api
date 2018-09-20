---
UID: NF:setupapi.SetupDiSetDriverInstallParamsA
title: SetupDiSetDriverInstallParamsA function
author: windows-sdk-content
description: The SetupDiSetDriverInstallParams function sets driver installation parameters for a driver information element.
old-location: devinst\setupdisetdriverinstallparams.htm
tech.root: devinst
ms.assetid: a6084bb4-f0c1-43f3-94e7-8fd0682f5ac0
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: SetupDiSetDriverInstallParams, SetupDiSetDriverInstallParams function [Device and Driver Installation], SetupDiSetDriverInstallParamsA, SetupDiSetDriverInstallParamsW, devinst.setupdisetdriverinstallparams, di-rtns_31ccb1b6-757d-48d0-b3bd-1c46ac3bc4bd.xml, setupapi/SetupDiSetDriverInstallParams
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiSetDriverInstallParamsA function


## -description


The <b>SetupDiSetDriverInstallParams</b> function sets driver installation parameters for a driver information element.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a> that contains a driver information element that represents the driver for which to set installation parameters.


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that specifies a device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be set to <b>NULL</b>. If this parameter is specified, <b>SetupDiSetDriverInstallParams</b> sets the driver installation parameters for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiSetDriverInstallParams</b> sets driver installation parameters for <i>DeviceInfoSet</i>. 


### -param DriverInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/13cdebad-6247-4651-a1d0-709e14af22f6">SP_DRVINFO_DATA</a> structure that specifies the driver for which installation parameters are set. If <i>DeviceInfoData</i> is specified, this driver must be a member of a driver list that is associated with <i>DeviceInfoData</i>. If <i>DeviceInfoData</i> is <b>NULL</b>, this driver must be a member of the global class driver list for <i>DeviceInfoSet</i>. 


### -param DriverInstallParams [in]

A pointer to an <a href="https://msdn.microsoft.com/300e636c-3f77-4d0b-9868-caaf92d87bfd">SP_DRVINSTALL_PARAMS</a> structure that specifies the new driver install parameters. 


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/7c5b0e3f-75cd-48e1-b84e-d81e4e4db7b2">SetupDiGetDriverInstallParams</a>
 

 


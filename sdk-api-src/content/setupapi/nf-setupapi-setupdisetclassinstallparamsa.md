---
UID: NF:setupapi.SetupDiSetClassInstallParamsA
title: SetupDiSetClassInstallParamsA function
author: windows-sdk-content
description: The SetupDiSetClassInstallParams function sets or clears class install parameters for a device information set or a particular device information element.
old-location: devinst\setupdisetclassinstallparams.htm
old-project: devinst
ms.assetid: a7f35e32-eaad-440b-8109-7320048ec7ba
ms.author: windowssdkdev
ms.date: 07/11/2018
ms.keywords: SetupDiSetClassInstallParams, SetupDiSetClassInstallParams function [Device and Driver Installation], SetupDiSetClassInstallParamsA, SetupDiSetClassInstallParamsW, devinst.setupdisetclassinstallparams, di-rtns_4bbd92e2-cdae-4b03-9b30-931b6155dc2c.xml, setupapi/SetupDiSetClassInstallParams
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
 - SetupDiSetClassInstallParams
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# SetupDiSetClassInstallParamsA function


## -description


The <b>SetupDiSetClassInstallParams</b> function sets or clears class install parameters for a device information set or a particular device information element. 


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> for which to set class install parameters.


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that represents the device for which to set class install parameters. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiSetClassInstallParams</b> sets the class installation parameters for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiSetClassInstallParams</b> sets the class install parameters that are associated with <i>DeviceInfoSet</i>.


### -param ClassInstallParams [in, optional]

A pointer to a buffer that contains the new class install parameters to use. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff552340">SP_CLASSINSTALL_HEADER</a> structure at the beginning of this buffer must have its <b>cbSize</b> field set to <b>sizeof(</b>SP_CLASSINSTALL_HEADER<b>)</b> and the <b>InstallFunction</b> field must be set to the DI_FUNCTION code that reflects the type of parameters contained in the rest of the buffer. 

If <i>ClassInstallParams</i> is not specified, the current class install parameters, if any, are cleared for the specified device information set or element.


### -param ClassInstallParamsSize [in]

The size, in bytes, of the <i>ClassInstallParams</i> buffer. If the buffer is not supplied (that is, the class install parameters are being cleared), <i>ClassInstallParamsSize</i> must be 0<i>.</i>


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



All parameters are validated before any changes are made. Therefore, a return value of <b>FALSE</b> indicates that no parameters were modified.

A side effect of setting class install parameters is that the DI_CLASSINSTALLPARAMS flag is set. If the caller wants to set the parameters, but disable their use, this flag must be cleared by a call to <b>SetupDiSetDeviceInstallParams</b>. 

If the class install parameters are cleared, the DI_CLASSINSTALLPARAMS flag is reset.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551083">SetupDiGetClassInstallParams</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552141">SetupDiSetDeviceInstallParams</a>
 

 


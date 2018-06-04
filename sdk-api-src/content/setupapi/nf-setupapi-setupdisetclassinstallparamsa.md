---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
 

 


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

# SetupDiGetClassInstallParamsW function


## -description


The <b>SetupDiGetClassInstallParams</b> function retrieves class installation parameters for a device information set or a particular device information element. 


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a> that contains the class install parameters to retrieve.


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specified a device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiGetClassInstallParams</b> retrieves the class installation parameters for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiGetClassInstallParams</b> retrieves the class install parameters for the global class driver list that is associated with <i>DeviceInfoSet</i>.


### -param ClassInstallParams [out, optional]

A pointer to a buffer that contains an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552340">SP_CLASSINSTALL_HEADER</a> structure. This structure must have its <b>cbSize</b> member set to <b>sizeof(</b>SP_CLASSINSTALL_HEADER<b>)</b> on input or the buffer is considered to be invalid. On output, the <b>InstallFunction</b> member is filled with the <a href="https://msdn.microsoft.com/f4aadd46-9651-45c3-bec5-65126a7fc9e7">device installation function code</a> for the class installation parameters being retrieved. If the buffer is large enough, it also receives the class installation parameters structure specific to the function code. If <i>ClassInstallParams</i> is not specified, <i>ClassInstallParamsSize</i> must be 0. 


### -param ClassInstallParamsSize [in]

The size, in bytes, of the <i>ClassInstallParams</i> buffer. If the buffer is supplied, it must be at least as large as <b>sizeof(</b>SP_CLASSINSTALL_HEADER<b>)</b>. If the buffer is not supplied, <i>ClassInstallParamsSize</i> must be 0<i>.</i>


### -param RequiredSize [out, optional]

A pointer to a variable of type DWORD that receives the number of bytes required to store the class install parameters. This parameter is optional and can be <b>NULL</b>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



The class install parameters are specific to a particular <a href="https://msdn.microsoft.com/f4aadd46-9651-45c3-bec5-65126a7fc9e7">device installation function code</a> that is stored in the <b>ClassInstallHeader</b> field located at the beginning of the <i>ClassInstallParams</i> buffer.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552122">SetupDiSetClassInstallParams</a>
 

 


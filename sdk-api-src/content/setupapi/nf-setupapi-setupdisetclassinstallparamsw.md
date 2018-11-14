---
UID: NF:setupapi.SetupDiSetClassInstallParamsW
title: SetupDiSetClassInstallParamsW function
author: windows-sdk-content
description: The SetupDiSetClassInstallParams function sets or clears class install parameters for a device information set or a particular device information element.
old-location: devinst\setupdisetclassinstallparams.htm
tech.root: devinst
ms.assetid: a7f35e32-eaad-440b-8109-7320048ec7ba
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: SetupDiSetClassInstallParams, SetupDiSetClassInstallParams function [Device and Driver Installation], SetupDiSetClassInstallParamsA, SetupDiSetClassInstallParamsW, devinst.setupdisetclassinstallparams, di-rtns_4bbd92e2-cdae-4b03-9b30-931b6155dc2c.xml, setupapi/SetupDiSetClassInstallParams
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
 - SetupDiSetClassInstallParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SetupDiSetClassInstallParamsW
: 
---

# SetupDiSetClassInstallParamsW function


## -description


The <b>SetupDiSetClassInstallParams</b> function sets or clears class install parameters for a device information set or a particular device information element. 


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> for which to set class install parameters.


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that represents the device for which to set class install parameters. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiSetClassInstallParams</b> sets the class installation parameters for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiSetClassInstallParams</b> sets the class install parameters that are associated with <i>DeviceInfoSet</i>.


### -param ClassInstallParams [in, optional]

A pointer to a buffer that contains the new class install parameters to use. The <a href="https://msdn.microsoft.com/9f76b741-d2a7-484d-94cb-b559b017399d">SP_CLASSINSTALL_HEADER</a> structure at the beginning of this buffer must have its <b>cbSize</b> field set to <b>sizeof(</b>SP_CLASSINSTALL_HEADER<b>)</b> and the <b>InstallFunction</b> field must be set to the DI_FUNCTION code that reflects the type of parameters contained in the rest of the buffer. 

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




<a href="https://msdn.microsoft.com/4ac1eb44-c7d6-48f3-bc7f-fb547e5a985e">SetupDiGetClassInstallParams</a>



<a href="https://msdn.microsoft.com/20384538-e124-41f7-94a6-c0fb9f5fe6a0">SetupDiSetDeviceInstallParams</a>
 

 


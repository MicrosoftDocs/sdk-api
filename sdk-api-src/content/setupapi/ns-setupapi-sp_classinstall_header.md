---
UID: NS:setupapi._SP_CLASSINSTALL_HEADER
title: SP_CLASSINSTALL_HEADER
author: windows-sdk-content
description: An SP_CLASSINSTALL_HEADER is the first member of any class install parameters structure. It contains the device installation request code that defines the format of the rest of the install parameters structure.
old-location: devinst\sp_classinstall_header.htm
tech.root: devinst
ms.assetid: 9f76b741-d2a7-484d-94cb-b559b017399d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSP_CLASSINSTALL_HEADER, PSP_CLASSINSTALL_HEADER, PSP_CLASSINSTALL_HEADER structure pointer [Device and Driver Installation], SP_CLASSINSTALL_HEADER, SP_CLASSINSTALL_HEADER structure [Device and Driver Installation], devinst.sp_classinstall_header, di-struct_96e0dbc0-fe54-4731-9ec7-0e633b521297.xml, setupapi/PSP_CLASSINSTALL_HEADER, setupapi/SP_CLASSINSTALL_HEADER"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - setupapi.h
api_name:
 - SP_CLASSINSTALL_HEADER
product: Windows
targetos: Windows
req.typenames: SP_CLASSINSTALL_HEADER, *PSP_CLASSINSTALL_HEADER
req.redist: 
---

# SP_CLASSINSTALL_HEADER structure


## -description


An SP_CLASSINSTALL_HEADER is the first member of any class install parameters structure. It contains the device installation request code that defines the format of the rest of the install parameters structure.


## -struct-fields




### -field cbSize

The size, in bytes, of the SP_CLASSINSTALL_HEADER structure. 


### -field InstallFunction

The device installation request (DIF code) for the class install parameters structure. 

DIF codes have the format DIF_<i>XXX</i> and are defined in <i>Setupapi.h</i>. See <a href="https://msdn.microsoft.com/f4aadd46-9651-45c3-bec5-65126a7fc9e7">Device Installation Function Codes</a> for a complete description of DIF codes.


## -remarks



When a component allocates a class install parameters structure, it typically initializes the header fields of the structure. Such a component sets the <b>InstallFunction</b> member to the DIF code for the installation request and sets <b>cbSize</b> to the size of the SP_CLASSINSTALL_HEADER structure. For example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>SP_REMOVEDEVICE_PARAMS RemoveDeviceParams;
RemoveDeviceParams.ClassInstallHeader.cbSize = sizeof(SP_CLASSINSTALL_HEADER);
RemoveDeviceParams.ClassInstallHeader.InstallFunction = DIF_REMOVE;</pre>
</td>
</tr>
</table></span></div>
A component must set the <b>InstallFunction</b> member before passing a class install parameters structure to <a href="https://msdn.microsoft.com/a7f35e32-eaad-440b-8109-7320048ec7ba">SetupDiSetClassInstallParams</a>. 

However, a component does not have to set this field when passing class install parameters to <a href="https://msdn.microsoft.com/4ac1eb44-c7d6-48f3-bc7f-fb547e5a985e">SetupDiGetClassInstallParams</a>. This function sets the <b>InstallFunction</b> member in the structure it passes back to the caller. It sets <b>InstallFunction</b> to the DIF_<i>XXX</i> code for the currently active device installation request.




## -see-also




<a href="https://msdn.microsoft.com/77682651-217f-4e3a-9d0e-0a93d315de53">SP_DETECTDEVICE_PARAMS</a>



<a href="https://msdn.microsoft.com/6410cdc3-5ec3-4fe1-8513-c0797b6a2582">SP_MOVEDEV_PARAMS</a>



<a href="https://msdn.microsoft.com/9e38ab29-af06-4ca4-b702-fdbed9cd54d4">SP_NEWDEVICEWIZARD_DATA</a>



<a href="https://msdn.microsoft.com/464919bb-c146-4d29-890f-c680a1aa06b2">SP_POWERMESSAGEWAKE_PARAMS</a>



<a href="https://msdn.microsoft.com/7c64d352-3b9f-4c52-96d5-1a627f6b54a3">SP_PROPCHANGE_PARAMS</a>



<a href="https://msdn.microsoft.com/08d3a5c7-9350-4fb3-8476-fb22e34d7054">SP_REMOVEDEVICE_PARAMS</a>



<a href="https://msdn.microsoft.com/7d1168dd-0b61-44fb-928d-38f2c57c1092">SP_SELECTDEVICE_PARAMS</a>



<a href="https://msdn.microsoft.com/f92e9aa4-ee29-4e69-be05-9c3c916197eb">SP_TROUBLESHOOTER_PARAMS</a>



<a href="https://msdn.microsoft.com/89f5e2a9-5336-421f-b781-688588695027">SP_UNREMOVEDEVICE_PARAMS</a>



<a href="https://msdn.microsoft.com/2aa631c3-8d00-4309-a37c-efaa7eda3efa">SetupDiCallClassInstaller</a>



<a href="https://msdn.microsoft.com/4ac1eb44-c7d6-48f3-bc7f-fb547e5a985e">SetupDiGetClassInstallParams</a>



<a href="https://msdn.microsoft.com/a7f35e32-eaad-440b-8109-7320048ec7ba">SetupDiSetClassInstallParams</a>
 

 


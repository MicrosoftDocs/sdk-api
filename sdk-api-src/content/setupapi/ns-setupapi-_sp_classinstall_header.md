---
UID: NS:setupapi._SP_CLASSINSTALL_HEADER
title: "_SP_CLASSINSTALL_HEADER"
author: windows-sdk-content
description: An SP_CLASSINSTALL_HEADER is the first member of any class install parameters structure. It contains the device installation request code that defines the format of the rest of the install parameters structure.
old-location: devinst\sp_classinstall_header.htm
old-project: devinst
ms.assetid: 9f76b741-d2a7-484d-94cb-b559b017399d
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: "*PSP_CLASSINSTALL_HEADER, PSP_CLASSINSTALL_HEADER, PSP_CLASSINSTALL_HEADER structure pointer [Device and Driver Installation], SP_CLASSINSTALL_HEADER, SP_CLASSINSTALL_HEADER structure [Device and Driver Installation], _SP_CLASSINSTALL_HEADER, devinst.sp_classinstall_header, di-struct_96e0dbc0-fe54-4731-9ec7-0e633b521297.xml, setupapi/PSP_CLASSINSTALL_HEADER, setupapi/SP_CLASSINSTALL_HEADER"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SP_CLASSINSTALL_HEADER, *PSP_CLASSINSTALL_HEADER
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
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _SP_CLASSINSTALL_HEADER structure


## -description


An SP_CLASSINSTALL_HEADER is the first member of any class install parameters structure. It contains the device installation request code that defines the format of the rest of the install parameters structure.


## -struct-fields




### -field cbSize

The size, in bytes, of the SP_CLASSINSTALL_HEADER structure. 


### -field InstallFunction

The device installation request (DIF code) for the class install parameters structure. 

DIF codes have the format DIF_<i>XXX</i> and are defined in <i>Setupapi.h</i>. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff541307">Device Installation Function Codes</a> for a complete description of DIF codes.


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
A component must set the <b>InstallFunction</b> member before passing a class install parameters structure to <a href="https://msdn.microsoft.com/library/windows/hardware/ff552122">SetupDiSetClassInstallParams</a>. 

However, a component does not have to set this field when passing class install parameters to <a href="https://msdn.microsoft.com/library/windows/hardware/ff551083">SetupDiGetClassInstallParams</a>. This function sets the <b>InstallFunction</b> member in the structure it passes back to the caller. It sets <b>InstallFunction</b> to the DIF_<i>XXX</i> code for the currently active device installation request.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552341">SP_DETECTDEVICE_PARAMS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553301">SP_MOVEDEV_PARAMS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553305">SP_NEWDEVICEWIZARD_DATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553311">SP_POWERMESSAGEWAKE_PARAMS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553315">SP_PROPCHANGE_PARAMS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553323">SP_REMOVEDEVICE_PARAMS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553326">SP_SELECTDEVICE_PARAMS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553341">SP_TROUBLESHOOTER_PARAMS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553349">SP_UNREMOVEDEVICE_PARAMS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550922">SetupDiCallClassInstaller</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551083">SetupDiGetClassInstallParams</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552122">SetupDiSetClassInstallParams</a>
 

 


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
 

 


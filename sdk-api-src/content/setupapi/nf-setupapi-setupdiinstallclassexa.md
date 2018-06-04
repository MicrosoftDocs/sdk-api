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

# SetupDiInstallClassExA function


## -description


The <b>SetupDiInstallClassEx</b> function installs a class installer or an interface class.


## -parameters




### -param hwndParent [in, optional]

The handle to the parent window for any user interface that is used to install this class. This parameter is optional and can be <b>NULL</b>.


### -param InfFileName [in, optional]

A pointer to a NULL-terminated string that contains the name of an INF file. This parameter is optional and can be <b>NULL</b>. If this function is being used to install a class installer, the INF file contains an <a href="devinst.inf_classinstall32_section">INF ClassInstall32 section</a> and this parameter must not be <b>NULL</b>.

If this function is being used to install an interface class, the INF file contains an <a href="devinst.inf_interfaceinstall32_section">INF InterfaceInstall32 section</a>. 


### -param Flags [in]

A value of type DWORD that controls the installation process. <i>Flags</i> can be zero or a bitwise OR of the following values:





#### DI_NOVCP

Set this flag if <i>FileQueue</i> is supplied. 

DI_NOVCP instructs the <b>SetupInstallFromInfSection</b> function not to create a queue of its own and to use the caller-supplied queue instead. 

If this flag is set, files are not copied just queued. 

For more information about the <b>SetupInstallFromInfSection</b> function, see the Microsoft Windows SDK documentation.



#### DI_NOBROWSE

Set this flag to disable browsing if a copy operation cannot find a specified file. If the caller supplies a file queue, this flag is ignored.



#### DI_FORCECOPY

Set this flag to always copy files, even if they are already present on the user's computer. If the caller supplies a file queue, this flag is ignored.



#### DI_QUIETINSTALL

Set this flag to suppress the user interface unless absolutely necessary. For example, do not display the progress dialog. If the caller supplies a file queue, this flag is ignored.


### -param FileQueue [in, optional]

If the DI_NOVCP flag is set, this parameter supplies a handle to a file queue where file operations should be queued but not committed.


### -param InterfaceClassGuid [in, optional]

A pointer to a GUID that identifies the interface class to be installed. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, this function is being used to install the interface class represented by the GUID. If this parameter is <b>NULL</b>, this function is being used to install a class installer.


### -param Reserved1

Reserved. Must be zero.


### -param Reserved2

Reserved. Must be zero.


## -returns



<b>SetupDiInstallClassEx</b> returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



The caller of this function must be a member of the Administrators group.

<b>SetupDiInstallClassEx</b> is typically called by a class installer to install a new <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> or a new <a href="https://msdn.microsoft.com/C989D2D3-E8DE-4D64-86EE-3D3B3906390D">device interface class</a>. 

<div class="alert"><b>Note</b>  An interface class can also be installed automatically by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff552043">SetupDiInstallDeviceInterfaces</a> to install the device interfaces for a device.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550922">SetupDiCallClassInstaller</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552043">SetupDiInstallDeviceInterfaces</a>
 

 


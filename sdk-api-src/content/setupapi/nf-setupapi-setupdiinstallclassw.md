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

# SetupDiInstallClassW function


## -description


The <b>SetupDiInstallClass</b> function installs the <b>ClassInstall32</b> section of the specified INF file.


## -parameters




### -param hwndParent [in, optional]

The handle to the parent window for any user interface that is used to install this class. This parameter is optional and can be <b>NULL</b>.


### -param InfFileName [in]

A pointer to a NULL-terminated string that contains the name of the INF file that contains an <a href="devinst.inf_classinstall32_section">INF ClassInstall32 section</a>.


### -param Flags [in]

These flags control the installation process. Can be a combination of the following:





#### DI_NOVCP

Set this flag if <i>FileQueue</i> is supplied. DI_NOVCP instructs the <b>SetupInstallFromInfSection</b> function (described in Microsoft Windows SDK documentation) not to create a queue of its own and to use the caller-supplied queue instead. If this flag is set, files are not copied just queued. 



#### DI_NOBROWSE

Set this flag to disable browsing if a copy operation cannot find a specified file. If the caller supplies a file queue, this flag is ignored.



#### DI_FORCECOPY

Set this flag to always copy files, even if they are already present on the user's computer. If the caller supplies a file queue, this flag is ignored.



#### DI_QUIETINSTALL

Set this flag to suppress the user interface unless absolutely necessary. For example, do not display the progress dialog. If the caller supplies a file queue, this flag is ignored.


### -param FileQueue [in, optional]

If the DI_NOVCP flag is set, this parameter supplies a handle to a file queue where file operations should be queued but not committed.


##### - Flags.DI_FORCECOPY

Set this flag to always copy files, even if they are already present on the user's computer. If the caller supplies a file queue, this flag is ignored.


##### - Flags.DI_NOBROWSE

Set this flag to disable browsing if a copy operation cannot find a specified file. If the caller supplies a file queue, this flag is ignored.


##### - Flags.DI_NOVCP

Set this flag if <i>FileQueue</i> is supplied. DI_NOVCP instructs the <b>SetupInstallFromInfSection</b> function (described in Microsoft Windows SDK documentation) not to create a queue of its own and to use the caller-supplied queue instead. If this flag is set, files are not copied just queued. 


##### - Flags.DI_QUIETINSTALL

Set this flag to suppress the user interface unless absolutely necessary. For example, do not display the progress dialog. If the caller supplies a file queue, this flag is ignored.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



The caller of this function must be a member of the Administrators group.

This function is called by a class installer when it installs a device of a new device class.

To install an interface class or a device class, use <a href="https://msdn.microsoft.com/library/windows/hardware/ff552032">SetupDiInstallClassEx</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550922">SetupDiCallClassInstaller</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552032">SetupDiInstallClassEx</a>
 

 


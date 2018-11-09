---
UID: NF:setupapi.SetupDiInstallClassA
title: SetupDiInstallClassA function
author: windows-sdk-content
description: The SetupDiInstallClass function installs the ClassInstall32 section of the specified INF file.
old-location: devinst\setupdiinstallclass.htm
tech.root: devinst
ms.assetid: 6709936b-cd44-444a-a0c0-14b5ebce5226
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: SetupDiInstallClass, SetupDiInstallClass function [Device and Driver Installation], SetupDiInstallClassA, SetupDiInstallClassW, devinst.setupdiinstallclass, di-rtns_9d55009f-08f3-448c-9c1e-468e995f8cb9.xml, setupapi/SetupDiInstallClass
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
 - SetupDiInstallClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiInstallClassA function


## -description


The <b>SetupDiInstallClass</b> function installs the <b>ClassInstall32</b> section of the specified INF file.


## -parameters




### -param hwndParent [in, optional]

The handle to the parent window for any user interface that is used to install this class. This parameter is optional and can be <b>NULL</b>.


### -param InfFileName [in]

A pointer to a NULL-terminated string that contains the name of the INF file that contains an <a href="https://msdn.microsoft.com/library/Ff546335(v=VS.85).aspx">INF ClassInstall32 section</a>.


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


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



The caller of this function must be a member of the Administrators group.

This function is called by a class installer when it installs a device of a new device class.

To install an interface class or a device class, use <a href="https://msdn.microsoft.com/72ab3fb4-dc4f-439a-87ed-4f4ad061d03a">SetupDiInstallClassEx</a>.




## -see-also




<a href="https://msdn.microsoft.com/2aa631c3-8d00-4309-a37c-efaa7eda3efa">SetupDiCallClassInstaller</a>



<a href="https://msdn.microsoft.com/72ab3fb4-dc4f-439a-87ed-4f4ad061d03a">SetupDiInstallClassEx</a>
 

 


---
UID: NF:setupapi.SetupDiOpenClassRegKeyExW
title: SetupDiOpenClassRegKeyExW function
author: windows-sdk-content
description: The SetupDiOpenClassRegKeyEx function opens the device setup class registry key, the device interface class registry key, or a specific class's subkey. This function opens the specified key on the local computer or on a remote computer.
old-location: devinst\setupdiopenclassregkeyex.htm
tech.root: devinst
ms.assetid: c931f906-8237-4203-b9b6-4dd54a93ca8b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SetupDiOpenClassRegKeyEx, SetupDiOpenClassRegKeyEx function [Device and Driver Installation], SetupDiOpenClassRegKeyExA, SetupDiOpenClassRegKeyExW, devinst.setupdiopenclassregkeyex, di-rtns_498e4805-8ce4-41cb-8d77-552dbf342f60.xml, setupapi/SetupDiOpenClassRegKeyEx
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
 - SetupDiOpenClassRegKeyEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiOpenClassRegKeyExW function


## -description


The <b>SetupDiOpenClassRegKeyEx</b> function opens the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> registry key, the <a href="https://msdn.microsoft.com/C989D2D3-E8DE-4D64-86EE-3D3B3906390D">device interface class</a> registry key, or a specific class's subkey. This function opens the specified key on the local computer or on a remote computer.


## -parameters




### -param ClassGuid [in, optional]

A pointer to the GUID of the class whose registry key is to be opened. This parameter is optional and can be <b>NULL</b>. If this parameter is <b>NULL</b>, the root of the class tree (<b>HKLM\SYSTEM\CurrentControlSet\Control\Class</b>) is opened.


### -param samDesired [in]

The registry security access for the key to be opened. For information about registry security access values of type REGSAM, see the Microsoft Windows SDK documentation. 


### -param Flags [in]

The type of registry key to be opened, which is specified by one of the following:





#### DIOCR_INSTALLER

Open a setup class key. If <i>ClassGuid</i> is <b>NULL</b>, open the root key of the class installer branch.



#### DIOCR_INTERFACE

Open an interface class key. If <i>ClassGuid</i> is <b>NULL</b>, open the root key of the interface class branch.


### -param MachineName [in, optional]

Optionally points to a string that contains the name of a remote computer on which to open the specified key.


### -param Reserved

Reserved. Must be <b>NULL</b>.


##### - Flags.DIOCR_INSTALLER

Open a setup class key. If <i>ClassGuid</i> is <b>NULL</b>, open the root key of the class installer branch.


##### - Flags.DIOCR_INTERFACE

Open an interface class key. If <i>ClassGuid</i> is <b>NULL</b>, open the root key of the interface class branch.


## -returns



<b>SetupDiOpenClassRegKeyEx</b> returns a handle to an opened registry key where information about this setup class can be stored/retrieved. 

If the function fails, it returns INVALID_HANDLE_VALUE. To get extended error information, call <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



Depending on the value that is passed in the <i>samDesired</i> parameter, it might be necessary for the caller of this function to be a member of the Administrators group.

<b>SetupDiOpenClassRegKeyEx</b> does not create a registry key if it does not already exist.

Callers of this function must close the handle returned from this function by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=194543">RegCloseKey</a>.




## -see-also




<a href="https://msdn.microsoft.com/1be942a1-428d-4cc4-bc9f-9f21243c3d21">SetupDiCreateDeviceInterfaceRegKey</a>



<a href="https://msdn.microsoft.com/ffa435c8-4a73-454e-be36-cd90ba6e6d11">SetupDiOpenDevRegKey</a>
 

 


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

# SetupDiOpenClassRegKey function


## -description


The <b>SetupDiOpenClassRegKey</b> function opens the setup class registry key or a specific class's subkey.


## -parameters




### -param ClassGuid [in, optional]

A pointer to the GUID of the setup class whose key is to be opened. This parameter is optional and can be <b>NULL</b>. If this parameter is <b>NULL</b>, the root of the setup class tree (<b>HKLM\SYSTEM\CurrentControlSet\Control\Class</b>) is opened.


### -param samDesired [in]

The registry security access for the key to be opened. For information about registry security access values of type REGSAM, see the Microsoft Windows SDK documentation. 


## -returns



If the function is successful, it returns a handle to an opened registry key where information about this setup class can be stored/retrieved. 

If the function fails, it returns INVALID_HANDLE_VALUE. To get extended error information, call <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



Depending on the value that is passed in the <i>samDesired</i> parameter, it might be necessary for the caller of this function to be a member of the Administrators group.

This function does not create a registry key if it does not already exist.

The handle returned from this function must be closed by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=194543">RegCloseKey</a>.

To open the interface class registry key or a specific interface class subkey, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff552067">SetupDiOpenClassRegKeyEx</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552067">SetupDiOpenClassRegKeyEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552079">SetupDiOpenDevRegKey</a>
 

 


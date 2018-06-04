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

# SetupDiGetHwProfileFriendlyNameExW function


## -description


The <b>SetupDiGetHwProfileFriendlyNameEx</b> function retrieves the friendly name associated with a hardware profile ID on a local or remote computer.


## -parameters




### -param HwProfile [in]

Supplies the hardware profile ID associated with the friendly name to retrieve. If this parameter is 0, the friendly name for the current hardware profile is retrieved.


### -param FriendlyName [out]

A pointer to a character buffer to receive the friendly name.


### -param FriendlyNameSize [in]

The size, in characters, of the <i>FriendlyName</i> buffer.


### -param RequiredSize [out, optional]

A pointer to a variable to receive the number of characters required to store the friendly name (including a NULL terminator). This parameter is optional and can be <b>NULL</b>.


### -param MachineName [in, optional]

A pointer to NULL-terminated string that contains the name of a remote computer on which the hardware profile ID resides. This parameter is optional and can be <b>NULL</b>. If <i>MachineName</i> is <b>NULL</b>, the hardware profile ID is on the local computer. 


### -param Reserved

Must be <b>NULL</b>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551983">SetupDiGetHwProfileFriendlyName</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552006">SetupDiGetHwProfileListEx</a>
 

 


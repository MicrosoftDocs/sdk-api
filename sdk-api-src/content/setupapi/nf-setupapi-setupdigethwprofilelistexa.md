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

# SetupDiGetHwProfileListExA function


## -description


The <b>SetupDiGetHwProfileListEx</b> function retrieves a list of all currently defined hardware profile IDs on a local or remote computer.


## -parameters




### -param HwProfileList [out]

A pointer to an array to receive the list of currently defined hardware profile IDs.


### -param HwProfileListSize [in]

The number of DWORDs in the <i>HwProfileList</i> buffer.


### -param RequiredSize [out]

A pointer to a variable of type DWORD that receives the number of hardware profiles that are currently defined. If the number is larger than <i>HwProfileListSize</i>, the list is truncated to fit the array size. The value returned in <i>RequiredSize</i> indicates the array size required to store the entire list of hardware profiles. 


### -param CurrentlyActiveIndex [out, optional]

A pointer to a variable that receives the index of the currently active hardware profile in the retrieved hardware profile list. This parameter is optional and can be <b>NULL</b>.


### -param MachineName [in, optional]

A pointer to a NULL-terminated string that contains the name of a remote system for which to retrieve the list of hardware profile IDs. This parameter is optional and can be <b>NULL</b>. If this parameter is <b>NULL</b>, the list is retrieved for the local system.


### -param Reserved

Must be <b>NULL</b>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>. If the required size is larger than <i>HwProfileListSize</i>, <b>SetupDiGetHwProfileListEx</b> returns <b>FALSE</b> and a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_INSUFFICIENT_BUFFER. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551989">SetupDiGetHwProfileFriendlyNameEx</a>
 

 


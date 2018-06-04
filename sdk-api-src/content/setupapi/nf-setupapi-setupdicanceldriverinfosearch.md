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

# SetupDiCancelDriverInfoSearch function


## -description


The <b>SetupDiCancelDriverInfoSearch</b> function cancels a driver list search that is currently in progress in a different thread. 


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> for which a driver list is being built.


## -returns



If a driver list search is underway for the specified device information set when this function is called, the search is terminated. <b>SetupDiCancelDriverInfoSearch</b> returns <b>TRUE</b> when the termination is confirmed. Otherwise, it returns <b>FALSE</b> and a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_INVALID_HANDLE. 




## -remarks



<b>SetupDiCancelDriverInfoSearch</b> is a synchronous call. Therefore, it does not return until the driver search thread responds to the termination request.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550917">SetupDiBuildDriverInfoList</a>
 

 


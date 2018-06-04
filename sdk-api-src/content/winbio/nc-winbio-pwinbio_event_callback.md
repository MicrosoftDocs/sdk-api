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

# PWINBIO_EVENT_CALLBACK callback function


## -description


Called by the Windows Biometric Framework to return results from the   asynchronous  <a href="https://msdn.microsoft.com/408291ca-66fe-4f4a-8f6e-3a1b60eb2d15">WinBioRegisterEventMonitor</a> function. The client application must implement this function.


## -parameters




### -param EventCallbackContext [in, optional]

Pointer to a buffer defined by the application and passed to the <i>EventCallbackContext</i> parameter of the <a href="https://msdn.microsoft.com/408291ca-66fe-4f4a-8f6e-3a1b60eb2d15">WinBioRegisterEventMonitor</a> function. The buffer is not modified by the framework or the biometric unit. Your application can use the data to help it determine what actions to perform or to maintain additional information about the biometric capture.


### -param OperationStatus [in]

Error code returned by the capture operation.


### -param Event [in]

Pointer to a WINBIO_EVENT value. For more information, see <a href="https://msdn.microsoft.com/73805413-a8d9-4682-aa21-7032451d750a">WINBIO_EVENT Constants</a>.


## -returns



Do not return a value from your implementation of this function.




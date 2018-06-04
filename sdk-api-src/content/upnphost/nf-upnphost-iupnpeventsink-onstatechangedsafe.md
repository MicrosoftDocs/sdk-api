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

# IUPnPEventSink::OnStateChangedSafe


## -description


The 
<b>OnStateChangedSafe</b> method sends an event to the device host with the list of DISPIDs that have changed. The device host must query the service object to obtain the new value for each state variable that has changed.

The 
<b>OnStateChangedSafe</b> method can only be used by Visual Basic developers and those using languages that do not support native arrays.


## -parameters




### -param varsadispidChanges [in]

Contains a safearray of the DISPIDs of the state variables that have changed.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/431423c9-2873-422d-a28c-c4ef23109114">IUPnPEventSink</a>
 

 


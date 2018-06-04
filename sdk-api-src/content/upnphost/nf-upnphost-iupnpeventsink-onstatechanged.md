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

# IUPnPEventSink::OnStateChanged


## -description


The 
<b>OnStateChanged</b> method sends an event to the device host with the list of DISPIDs of the state variables that have changed. The device host must query the service object to obtain the new value for each state variable that has changed.

This method is unavailable to Visual Basic developers, and those using other languages that do not support native arrays. These developers must use 
<a href="https://msdn.microsoft.com/95792229-287c-43f1-b03a-45aa63a9682f">OnStateChangedSafe</a> instead.


## -parameters




### -param cChanges [in]

Specifies the number of variables in <i>rgdispidChanges</i>. The value indicates the number of variables whose values have changed.


### -param rgdispidChanges [in]

Contains a list of the DISPIDs of the state variables that have changed. The number of elements in this buffer is specified by <i>cChanges</i>.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

If <i>cChanges</i> is zero or <i>rgdispidChanges</i> is <b>NULL</b>, E_INVALIDARG is returned.




## -see-also




<a href="https://msdn.microsoft.com/431423c9-2873-422d-a28c-c4ef23109114">IUPnPEventSink</a>
 

 


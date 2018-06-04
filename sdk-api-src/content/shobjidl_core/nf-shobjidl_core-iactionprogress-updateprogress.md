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

# IActionProgress::UpdateProgress


## -description



      Updates the progress of an action to the UI.


## -parameters




### -param ulCompleted [in]

Type: <b>ULONGLONG</b>

The amount of the action completed.


### -param ulTotal [in]

Type: <b>ULONGLONG</b>

The total amount of the action.


## -returns



Type: <b>HRESULT</b>

Return S_OK if successful, or an error value otherwise.




## -remarks




			This method should be called periodically to update the progress of the action. The implementing class may interpret these values in any way desired, although the values of <i>ulCompleted</i> and <i>ulTotal</i> should be interpreted relative to one another to determine a meaningful progress amount. Often, a percentage is desired, in which case the value of <i>ulCompleted</i> should be divided by <i>ulTotal</i>, and the result multiplied by a value of 100.
			




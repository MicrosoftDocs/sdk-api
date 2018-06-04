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

# IATSCLocator::get_TSID


## -description



The <b>get_TSID</b> method retrieves the transport stream ID.




## -parameters




### -param TSID






#### - pTSID [out]

Receives the transport stream ID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This property is not required for tuning. It will be set by the BDA Transport Information Filter (TIF) when the signal is acquired. This property is not used by the application but may be used by one or more of the receiver filters. For example, a TIF may use this to determine whether the transport stream has changed from what was originally tuned and generate events that cause re-acquisition of the requested program.




## -see-also




<a href="https://msdn.microsoft.com/8ca7d50f-e7cc-4938-a2ed-fce5278b73fd">IATSCLocator Interface</a>
 

 


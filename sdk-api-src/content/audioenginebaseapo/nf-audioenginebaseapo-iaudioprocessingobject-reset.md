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

# IAudioProcessingObject::Reset


## -description


The Reset method resets the APO to its original state. This method does not cause any changes in the connection objects that are attached to the input or the output of the APO.


## -parameters






#### - None

None


## -returns



The <code>Reset</code> method returns a value of S_OK when the call is completed successfully.




## -remarks



This method is not real-time compliant and must not be called from a real-time processing thread. The implementation of this method does not and must not touch paged memory. Additionally, it must not call any blocking system routines.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536501">IAudioProcessingObject</a>
 

 


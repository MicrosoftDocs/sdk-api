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

# MI_Application_NewDestinationOptions function


## -description


Creates an <a href="https://msdn.microsoft.com/7f835ff4-3917-497c-bfe9-ca335cc35938">MI_DestinationOptions</a> object that can be used with the <a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a>  function.


## -parameters




### -param application [in]

Handle returned from <a href="https://msdn.microsoft.com/32696A33-820D-4D01-AF71-DDA1F34EFBE0">MI_Application_Initialize</a>.


### -param options [out]

Options container that is returned from this function.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



Destination options are used to store the configuration associated with connecting to the destination computer.  The available options can vary depending on the underlying protocol.  If the session and operations on that session just need to work with the current thread identity (or process if thread is not impersonating), then additional settings may not be needed.

Options must be closed by a call to <a href="https://msdn.microsoft.com/c4cc8622-1adb-4e91-877f-11a260ca4bd7">MI_DestinationOptions_Delete</a>.




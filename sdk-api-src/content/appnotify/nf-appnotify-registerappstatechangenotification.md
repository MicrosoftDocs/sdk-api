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

# RegisterAppStateChangeNotification function


## -description


Enables an app to register a callback function through which it can be notified that its library is going into or coming out of a suspended state. The app can use this information to perform any necessary operations, such as preserving state, that should be performed at that point.


## -parameters




### -param Routine [in]

A pointer to a callback function that is called when the app enters or leaves the suspended state. See <a href="https://msdn.microsoft.com/AA5B09FA-2016-4C9D-8DE3-CD3C6141B45A">PAPPSTATE_CHANGE_ROUTINE</a> for more detail on this function.


### -param Context [in, optional]

App-specific context information that the app uses when going into or out of a suspended state. This is commonly a "this" pointer.


### -param Registration [out]

When this function returns successfully, this parameter receives the address of a pointer to a value that can be used to identify the registration. Store this value to use with <a href="https://msdn.microsoft.com/97D92C75-5C73-4DCF-BE65-2558A1101789">UnregisterAppStateChangeNotification</a>.


## -returns



A standard Win32 status code.




## -see-also




<a href="https://msdn.microsoft.com/97D92C75-5C73-4DCF-BE65-2558A1101789">UnregisterAppStateChangeNotification</a>
 

 


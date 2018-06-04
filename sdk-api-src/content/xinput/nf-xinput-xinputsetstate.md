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

# XInputSetState function


## -description


Sends data to a connected controller. This function is used to activate the vibration function of a controller.


## -parameters




### -param dwUserIndex [in]

Index of the user's controller. Can be a value from 0 to 3. For information about how this value is determined and how the value maps to indicators on the controller, see <a href="getting_started_with_xinput.htm">Multiple Controllers</a>.


### -param pVibration [in, out]

Pointer to an <a href="https://msdn.microsoft.com/134A22DD-95DA-4270-AC42-93C7EF110A3A">XINPUT_VIBRATION</a> structure containing the vibration information to send to the controller.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the controller is not connected, the return value is <b>ERROR_DEVICE_NOT_CONNECTED</b>.

If the function fails, the return value is an error code defined in WinError.h. The function does not use <i>SetLastError</i> to set the calling thread's last-error code.




## -see-also




<a href="https://msdn.microsoft.com/134A22DD-95DA-4270-AC42-93C7EF110A3A">XINPUT_VIBRATION</a>



<a href="https://msdn.microsoft.com/c1533555-9094-0030-f025-6f47e9002e1a">XInput Functions</a>



<a href="https://msdn.microsoft.com/D261219D-0175-4690-8F1F-BDAACE2E7424">XInputGetState</a>
 

 


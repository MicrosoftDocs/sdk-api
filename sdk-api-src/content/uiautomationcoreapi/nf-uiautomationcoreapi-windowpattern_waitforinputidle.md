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

# WindowPattern_WaitForInputIdle function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Causes the calling code to block for the specified time or until the associated process enters an idle state, whichever completes first.


## -parameters




### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

The control pattern object.


### -param milliseconds [in]

Type: <b>int</b>

The number of milliseconds to wait before retrieving <i>pResult</i>.


### -param pResult [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

<b>TRUE</b> if the window is ready to accept user input; otherwise <b>FALSE</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




## -remarks




            This method is typically used in conjunction with the handling of a WindowOpenedEvent 
        (<i>Window_WindowOpened_Event_GUID</i>).
        The implementation is dependent on the underlying application framework; 
        therefore this method may return some time after the window is ready for user input. 
        The calling code should not rely on this method to ascertain exactly when the window has become idle. 
        Use the value of <i>pResult</i> to determine if the window is ready for input or if the method timed out.






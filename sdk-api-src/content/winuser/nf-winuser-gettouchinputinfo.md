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

# GetTouchInputInfo function


## -description


Retrieves detailed information about touch inputs associated with a particular touch input handle.


## -parameters




### -param hTouchInput [in]

The touch input handle received in the <b>LPARAM</b> of a touch message. The function fails with <b>ERROR_INVALID_HANDLE</b> if this handle is not valid. Note that the handle is not valid after it has been used in a successful call to <a href="https://msdn.microsoft.com/bdc8bb94-3126-4183-9dfd-ba4844d98f29">CloseTouchInputHandle</a> or after it has been passed to <a href="https://msdn.microsoft.com/9fba2013-17a3-499c-80dc-627e89c0edaf">DefWindowProc, PostMessage, SendMessage</a> or one of their variants.


### -param cInputs [in]

The number of structures in the <i>pInputs</i> array. This should ideally be at least equal to the number of touch points associated with the message as indicated in the message <b>WPARAM</b>. If <i>cInputs</i> is less than the number of touch points, the function will still succeed and populate the <i>pInputs</i> buffer with information about <i>cInputs</i> touch points.


### -param pInputs [out]

A pointer to an array of <a href="https://msdn.microsoft.com/fc382759-3a1e-401e-a6a7-1bf209a5434b">TOUCHINPUT</a> structures to receive information about the touch points associated with the specified touch input handle.


### -param cbSize [in]

The size, in bytes, of a single <a href="https://msdn.microsoft.com/fc382759-3a1e-401e-a6a7-1bf209a5434b">TOUCHINPUT</a> structure. If <i>cbSize</i> is not the size of a single <b>TOUCHINPUT</b> structure, the function fails with <b>ERROR_INVALID_PARAMETER</b>.


## -returns



If the function succeeds, the return value is nonzero.
If the function fails, the return value is zero. To get extended error information, use the <a href="http://msdn.microsoft.com/en-us/library/ms679360.aspx">GetLastError</a> function.




## -remarks




      Calling <a href="https://msdn.microsoft.com/bdc8bb94-3126-4183-9dfd-ba4844d98f29">CloseTouchInputHandle</a> will not free memory associated with values retrieved in a call to <b>GetTouchInputInfo</b>.  Values in structures passed to <b>GetTouchInputInfo</b>  will be valid until you delete them.




## -see-also




<a href="https://msdn.microsoft.com/bdc8bb94-3126-4183-9dfd-ba4844d98f29">CloseTouchInputHandle</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/fc382759-3a1e-401e-a6a7-1bf209a5434b">TOUCHINPUT</a>
 

 


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

# CloseTouchInputHandle function


## -description


Closes a touch input handle, frees process memory associated with it, and invalidates the handle.


## -parameters




### -param hTouchInput [in]

The touch input handle received in the <b>LPARAM</b> of a touch message. The function fails with <b>ERROR_INVALID_HANDLE</b> if this handle is not valid. Note that the handle is not valid after it has been used in a successful call to <b>CloseTouchInputHandle</b> or after it has been passed to <a href="https://msdn.microsoft.com/9fba2013-17a3-499c-80dc-627e89c0edaf">DefWindowProc, PostMessage, SendMessage</a> or one of their variants.


## -returns



If the function succeeds, the return value is nonzero.
     



If the function fails, the return value is zero. To get extended error information, use the <a href="http://msdn.microsoft.com/en-us/library/ms679360.aspx">GetLastError</a> function.




## -remarks




      Calling <b>CloseTouchInputHandle</b> will not free memory associated with values retrieved in a call to <a href="https://msdn.microsoft.com/18caab11-9c22-46ac-b89f-dd3e662bea1e">GetTouchInputInfo</a>. Values in structures passed to <b>GetTouchInputInfo</b>  will be valid until you delete them.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/18caab11-9c22-46ac-b89f-dd3e662bea1e">GetTouchInputInfo</a>
 

 


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

# ImmRequestMessageW function


## -description


Generates a <a href="https://msdn.microsoft.com/c5e9f256-eed2-46cb-bb33-0e640a975f1f">WM_IME_REQUEST</a> message.


## -parameters




### -param HIMC

TBD


### -param WPARAM

TBD


### -param LPARAM

TBD




#### - hIMC [in]

Handle to the target input context.


#### - lParam [in]

Value of the <i>lParam</i> parameter for the <a href="https://msdn.microsoft.com/c5e9f256-eed2-46cb-bb33-0e640a975f1f">WM_IME_REQUEST</a> message.


#### - wParam [in]

Value of the <i>wParam</i> parameter for the <a href="https://msdn.microsoft.com/c5e9f256-eed2-46cb-bb33-0e640a975f1f">WM_IME_REQUEST</a> message.


## -returns



Returns an operation-specific value if successful, or 0 otherwise.




## -remarks



IME must use this function instead of sending the <a href="https://msdn.microsoft.com/c5e9f256-eed2-46cb-bb33-0e640a975f1f">WM_IME_REQUEST</a> message to the application in a call to <a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a>.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>



<a href="https://msdn.microsoft.com/c5e9f256-eed2-46cb-bb33-0e640a975f1f">WM_IME_REQUEST</a>
 

 


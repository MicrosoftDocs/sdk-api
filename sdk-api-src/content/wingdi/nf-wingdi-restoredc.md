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

# RestoreDC function


## -description


The <b>RestoreDC</b> function restores a device context (DC) to the specified state. The DC is restored by popping state information off a stack created by earlier calls to the <a href="https://msdn.microsoft.com/f438cd7f-436f-436c-b32e-67f5558740cb">SaveDC</a> function.


## -parameters




### -param hdc [in]

A handle to the DC.


### -param nSavedDC [in]

The saved state to be restored. If this parameter is positive, <i>nSavedDC</i> represents a specific instance of the state to be restored. If this parameter is negative, <i>nSavedDC</i> represents an instance relative to the current state. For example, -1 restores the most recently saved state.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



 Each DC maintains a stack of saved states. The <a href="https://msdn.microsoft.com/f438cd7f-436f-436c-b32e-67f5558740cb">SaveDC</a> function pushes the current state of the DC onto its stack of saved states. That state can be restored only to the same DC from which it was created. After a state is restored, the saved state is destroyed and cannot be reused. Furthermore, any states saved after the restored state was created are also destroyed and cannot be used. In other words, the <b>RestoreDC</b> function pops the restored state (and any subsequent states) from the state information stack.




## -see-also




<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/f438cd7f-436f-436c-b32e-67f5558740cb">SaveDC</a>
 

 


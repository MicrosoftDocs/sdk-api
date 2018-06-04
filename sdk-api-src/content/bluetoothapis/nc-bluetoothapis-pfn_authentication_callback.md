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

# PFN_AUTHENTICATION_CALLBACK callback function


## -description


The <b>PFN_AUTHENTICATION_CALLBACK</b> function is a callback function prototype used in conjunction with the <a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a> function.
<div class="alert"><b>Note</b>  When developing for Windows Vista SP2 and Windows 7 the use of <a href="https://msdn.microsoft.com/835a624f-c08d-402c-940b-4443e1b38d58">PFN_AUTHENTICATION_CALLBACK_EX</a> is recommended.</div><div> </div>

## -parameters




### -param pvParam

Optional. A context pointer previously passed into the <a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a> function.


### -param pDevice

A remote Bluetooth device requesting authentication. The remote address is the same address used to register the callback during the previous call to the <a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a> function.


## -returns



The return value from this function is ignored by the system.




## -remarks



A caller can register for multiple addresses with the same callback function.




## -see-also




<a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a>
 

 


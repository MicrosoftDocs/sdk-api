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

# IAMResourceControl::Reserve


## -description



The <code>Reserve</code> method reserves or unreserves a device resource.




## -parameters




### -param dwFlags [in]

Flag indicating whether to reserve or unreserve this device. The value must be a member of the <a href="https://msdn.microsoft.com/528c4e2e-2045-45a1-b502-75e103745c93">AMRESCTL_RESERVEFLAGS</a> enumeration.


### -param pvReserved [in]

Must be <b>NULL</b>.


## -returns



Returns S_OK if the device was successfully reserved or unreserved, S_FALSE if the device is currently reserved and will continue to be held, or an <b>HRESULT</b> error code if the device can't be reserved.




## -remarks



A resource can be reserved multiple times. If the method returns S_OK, the filter increments an internal reserve count. For every call to reserve a device that returns S_OK, the caller must make a matching call to unreserve the device.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9b0b6b46-bf61-44c2-981a-44df4d7c6dfb">IAMResourceControl Interface</a>
 

 


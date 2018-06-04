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

# DrvDeleteDeviceBitmap function


## -description


The <b>DrvDeleteDeviceBitmap</b> function deletes a device bitmap created by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556185">DrvCreateDeviceBitmap</a>.


## -parameters




### -param dhsurf

Handle to the bitmap to be deleted. This handle identifies the bitmap created by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556185">DrvCreateDeviceBitmap</a>.


## -returns



None




## -remarks



A driver must implement <b>DrvDeleteDeviceBitmap</b> if it supplies <a href="https://msdn.microsoft.com/library/windows/hardware/ff556185">DrvCreateDeviceBitmap</a>.

The driver should free any resources associated with the device bitmap.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556185">DrvCreateDeviceBitmap</a>
 

 


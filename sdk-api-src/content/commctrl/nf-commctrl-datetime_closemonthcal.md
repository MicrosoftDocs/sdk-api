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

# DateTime_CloseMonthCal macro


## -description


Closes the date and time picker (DTP) control. Use this macro or send the <a href="https://msdn.microsoft.com/f60af77f-ec34-4f3d-9427-cda7ac6083bf">DTM_CLOSEMONTHCAL</a> message explicitly.


## -parameters




### -param hdp

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the DTP control.


## -remarks



Destroys the control and sends a <a href="https://msdn.microsoft.com/94ace714-55cc-4c59-8b87-8d0348b15f34">DTN_CLOSEUP</a> notification that the control is closing—as opposed to the control is opening (dropping-down as in the <a href="https://msdn.microsoft.com/6f20fa87-2223-4876-b77d-2c684685bf10">DTN_DROPDOWN</a> notification)—to the control's parent.




## -see-also




<a href="https://msdn.microsoft.com/94ace714-55cc-4c59-8b87-8d0348b15f34">DTN_CLOSEUP</a>



<a href="https://msdn.microsoft.com/6f20fa87-2223-4876-b77d-2c684685bf10">DTN_DROPDOWN</a>



<b>Reference</b>
 

 


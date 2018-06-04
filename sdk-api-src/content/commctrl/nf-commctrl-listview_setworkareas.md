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

# ListView_SetWorkAreas macro


## -description


Sets the working areas within a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/87ac192d-f481-43ac-b8a5-c754cf33e487">LVM_SETWORKAREAS</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param nWorkAreas

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

The number of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structures in the array at 
					<i>lprc</i>. The maximum number of working areas allowed is defined by the <b>LV_MAX_WORKAREAS</b> value.


### -param prc

TBD






#### - hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


#### - lprc

Type: <b>LPRECT</b>

A pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structures that contain the new working areas of the list-view control. Values in these structures are in client coordinates. If this parameter is <b>NULL</b>, the working area will be set to the client area of the control. <i>nWorkAreas</i> specifies the number of structures in this array. 


## -see-also




<a href="https://msdn.microsoft.com/6953cdfc-8c59-4c6d-8998-f828cea3a315">Using List-View Controls</a>
 

 


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

# Header_SetOrderArray macro


## -description


Sets the left-to-right order of header items. You can use this macro or send the <a href="https://msdn.microsoft.com/094c424f-10bd-484d-8236-937811b703a6">HDM_SETORDERARRAY</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param iCount

TBD


### -param lpi

TBD






#### - hwndHD

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a header control. 


#### - iSize

Type: <b>int</b>

The size of the buffer at 
					<i>lpiArray</i>, in elements. This value must equal the value returned by <a href="https://msdn.microsoft.com/0e6d2131-53b4-4927-bd0f-577b8eaf237a">HDM_GETITEMCOUNT</a>. 


#### - lpiArray

Type: <b>int*</b>

A pointer to an array that specifies the order in which items should be displayed, from left to right. For example, if the contents of the array are {2,0,1}, the control displays item 2, item 0, and item 1, from left to right. 


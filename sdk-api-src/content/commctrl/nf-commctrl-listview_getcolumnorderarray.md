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

# ListView_GetColumnOrderArray macro


## -description


Gets the current left-to-right order of columns in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/d4636aa8-c61e-4467-abc7-eea897bf370e">LVM_GETCOLUMNORDERARRAY</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param iCount

Type: <b>int</b>

The number of columns in the list-view control.


### -param pi

TBD






#### - hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


#### - lpiArray

Type: <b>int*</b>

A pointer to an array of integers that will receive the index values of the columns in the list-view control. The array must be large enough to hold 
					<i>iCount</i> elements. 


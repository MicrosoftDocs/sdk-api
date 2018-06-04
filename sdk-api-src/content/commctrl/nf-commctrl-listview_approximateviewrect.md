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

# ListView_ApproximateViewRect macro


## -description


Calculates the approximate width and height required to display a given number of items. You can use this macro or send the <a href="https://msdn.microsoft.com/a14331a8-217d-48c6-9489-fb90c4d31b91">LVM_APPROXIMATEVIEWRECT</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param iWidth

TBD


### -param iHeight

TBD


### -param iCount

Type: <b>int</b>

The number of items to be displayed in the control. If this parameter is -1, the message uses the total number of items in the control.


#### - cx

Type: <b>int</b>

The proposed x-dimension of the control, in pixels. This parameter can be -1 to allow the message to use the current width value. 


#### - cy

Type: <b>int</b>

The proposed y-dimension of the control, in pixels. This parameter can be -1 to allow the message to use the current height value. 


#### - hwndLV

Type: <b>hwndLV</b>

A handle to the list-view control. 


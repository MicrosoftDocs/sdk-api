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

# Header_SetItem macro


## -description


Sets the attributes of the specified item in a header control. You can use this macro or send the <a href="https://msdn.microsoft.com/c8f0d526-3ebe-48c5-8aea-ea3703e2d983">HDM_SETITEM</a> message explicitly. 


## -parameters




### -param hwndHD

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a header control. 


### -param i

TBD


### -param phdi

TBD






#### - iIndex

Type: <b>int</b>

The current index of the item whose attributes are to be changed. 


#### - phdItem

Type: <b>LPHDITEM</b>

A pointer to an <a href="https://msdn.microsoft.com/2a717394-9123-409d-bda9-8e4ac6534101">HDITEM</a> structure that contains item information. When this message is sent, the 
					<b>mask</b> member of the structure must be set to indicate which attributes are being set. 


## -remarks



The <a href="https://msdn.microsoft.com/2a717394-9123-409d-bda9-8e4ac6534101">HDITEM</a> structure that supports this macro supports item order and image list information. By using these members, you can control the order in which items are displayed and specify images to appear with items. 




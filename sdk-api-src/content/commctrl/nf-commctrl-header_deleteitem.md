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

# Header_DeleteItem macro


## -description


Deletes an item from a header control. You can use this macro or send the <a href="https://msdn.microsoft.com/1dd1f233-2812-41ae-8a36-c42b9ac70ffc">HDM_DELETEITEM</a> message explicitly. 


## -parameters




### -param hwndHD

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the header control. 


### -param i

TBD






#### - index

Type: <b>int</b>

An index of the item to delete. 


## -remarks



The <b>Header_DeleteItem</b> macro is defined as follows. 

<pre class="syntax" xml:space="preserve"><code>#define Header_DeleteItem(hwndHD, index)     \

      (BOOL)SendMessage((hwndHD), HDM_DELETEITEM, (WPARAM)(int)(index), 0L)</code></pre>



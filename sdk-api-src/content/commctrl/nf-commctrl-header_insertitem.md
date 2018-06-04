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

# Header_InsertItem macro


## -description


Inserts a new item into a header control. You can use this macro or send the <a href="https://msdn.microsoft.com/aececf32-090d-4cd4-a239-4435a322f72e">HDM_INSERTITEM</a> message explicitly. 


## -parameters




### -param hwndHD

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the header control. 


### -param i

TBD


### -param phdi

Type: <b>const LPHDITEM</b>

A pointer to an <a href="https://msdn.microsoft.com/2a717394-9123-409d-bda9-8e4ac6534101">HDITEM</a> structure that contains information about the new item. 


#### - index

Type: <b>int</b>

The index of the item after which the new item is to be inserted. The new item is inserted at the end of the header control if 
					<i>index</i> is greater than or equal to the number of items in the control. If 
					<i>index</i> is zero, the new item is inserted at the beginning of the header control. 


## -remarks



The <b>Header_InsertItem</b> macro is defined as follows: 

<pre class="syntax" xml:space="preserve"><code>#define Header_InsertItem(hwndHD, index, phdi) \

    (int)SendMessage((hwndHD), HDM_INSERTITEM, (WPARAM)(int)(index), \

    (LPARAM)(const LPHDITEM)(phdi))</code></pre>



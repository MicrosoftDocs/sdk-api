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

# Header_GetItem macro


## -description


Gets information about an item in a header control. You can use this macro or send the <a href="https://msdn.microsoft.com/fb1330d3-fd28-490c-9caa-4b2b5ff86ba0">HDM_GETITEM</a> message explicitly. 


## -parameters




### -param hwndHD

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the header control. 


### -param i

TBD


### -param phdi

Type: <b>LPHDITEM</b>

A pointer to an <a href="https://msdn.microsoft.com/2a717394-9123-409d-bda9-8e4ac6534101">HDITEM</a> structure. When the message is sent, the <b>mask</b> member indicates the type of information being requested. When the message returns, the other members receive the requested information. If the 
<b>mask</b> member specifies zero, the message returns <b>TRUE</b> but copies no information to the structure. 


#### - index

Type: <b>int</b>

The index of the item for which information is to be retrieved. 


## -remarks



If the HDI_TEXT flag is set in the 
				<b>mask</b> member of the <a href="https://msdn.microsoft.com/2a717394-9123-409d-bda9-8e4ac6534101">HDITEM</a> structure, the control may change the 
				<b>pszText</b> member of the structure to point to the new text instead of filling the buffer with the requested text. Applications should not assume that the text will always be placed in the requested buffer.

The <b>Header_GetItem</b> macro is defined as follows:

<pre class="syntax" xml:space="preserve"><code>#define Header_GetItem(hwndHD, index, phdi)      \

    (BOOL)SendMessage((hwndHD), HDM_GETITEM,   \

    (WPARAM)(int)(index), (LPARAM)(LPHDITEM)(phdi))</code></pre>



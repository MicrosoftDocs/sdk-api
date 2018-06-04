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

# Header_Layout macro


## -description


Retrieves the correct size and position of a header control within the parent window. You can use this macro or send the <a href="https://msdn.microsoft.com/0763e483-f01d-4739-8c61-1c52d1aad0b4">HDM_LAYOUT</a> message explicitly. 


## -parameters




### -param hwndHD [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the header control. 


### -param playout [out]

Type: <b>LPHDLAYOUT</b>

A pointer to an <a href="https://msdn.microsoft.com/630a9d76-6143-44bb-ac8b-1f55c31385cc">HDLAYOUT</a> structure. The 
					<b>prc</b> member specifies the coordinates of a rectangle, and the 
					<b>pwpos</b> member receives the size and position for the header control within the rectangle. 


## -remarks



The <b>Header_Layout</b> macro is defined as follows: 

<pre class="syntax" xml:space="preserve"><code>#define Header_Layout(hwndHD, playout) \

    (BOOL)SendMessage((hwndHD), HDM_LAYOUT, 0, \

    (LPARAM)(LPHDLAYOUT)(playout))</code></pre>



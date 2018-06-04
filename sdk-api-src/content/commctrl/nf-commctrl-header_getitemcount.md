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

# Header_GetItemCount macro


## -description


Gets a count of the items in a header control. You can use this macro or send the <a href="https://msdn.microsoft.com/0e6d2131-53b4-4927-bd0f-577b8eaf237a">HDM_GETITEMCOUNT</a> message explicitly. 


## -parameters




### -param hwndHD

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the header control. 


## -remarks



The <b>Header_GetItemCount</b> macro is defined as follows. 

<pre class="syntax" xml:space="preserve"><code>#define Header_GetItemCount(hwndHD)   \

       (int)SendMessage((hwndHD), HDM_GETITEMCOUNT, 0, 0L)</code></pre>



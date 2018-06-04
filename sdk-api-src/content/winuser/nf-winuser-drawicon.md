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

# DrawIcon function


## -description


Draws an icon or cursor into the specified device context.

To specify additional drawing options, use the <a href="https://msdn.microsoft.com/037005b4-e9b2-483a-b277-7abd53a44b99">DrawIconEx</a> function.


## -parameters




### -param hDC [in]

Type: <b>HDC</b>

A handle to the device context into which the icon or cursor will be drawn. 


### -param X [in]

Type: <b>int</b>

The logical x-coordinate of the upper-left corner of the icon. 


### -param Y [in]

Type: <b>int</b>

The logical y-coordinate of the upper-left corner of the icon. 


### -param hIcon [in]

Type: <b>HICON</b>

A handle to the icon to be drawn. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<b>DrawIcon</b> places the icon's upper-left corner at the location specified by the <i>X</i> and <i>Y</i> parameters. The location is subject to the current mapping mode of the device context. 

<b>DrawIcon</b> draws the icon or cursor using the width and height specified by the system metric values for icons; for more information, see <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a>.


#### Examples

For an example, see <a href="using_icons.htm">Displaying an Icon</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/73497232-fb99-4b9c-9ccb-575a9a6ece56">CreateIcon</a>



<a href="https://msdn.microsoft.com/037005b4-e9b2-483a-b277-7abd53a44b99">DrawIconEx</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a>



<b>Reference</b>
 

 


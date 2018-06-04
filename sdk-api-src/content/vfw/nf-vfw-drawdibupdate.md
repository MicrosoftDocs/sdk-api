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

# DrawDibUpdate macro


## -description



The <b>DrawDibUpdate</b> macro draws the last frame in the DrawDib off-screen buffer.




## -parameters




### -param hdd

Handle to a DrawDib DC. 


### -param hdc

Handle of the DC. 


### -param x

TBD


### -param y

TBD






#### - xDst

The x-coordinate, in MM_TEXT client coordinates, of the upper left corner of the destination rectangle. 


#### - yDst

The y-coordinate, in MM_TEXT client coordinates, of the upper left corner of the destination rectangle. 


## -remarks



The <b>DrawDibUpdate</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define DrawDibUpdate( hdd, hdc, x, y) \ 
    DrawDibDraw( hdd, hdc, x, y, 0, 0, NULL, NULL, 0, 0, \ 
    0, 0, DDF_UPDATE) 
</pre>
</td>
</tr>
</table></span></div>
This macro can be used to refresh an image or a portion of an image displayed by your application.




## -see-also




<a href="https://msdn.microsoft.com/22c3e86f-8b7b-42f9-afec-8df95f0a8a9e">DrawDib Macros</a>
 

 


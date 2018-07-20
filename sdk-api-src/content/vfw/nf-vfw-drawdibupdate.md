---
UID: NF:vfw.DrawDibUpdate
title: DrawDibUpdate macro
author: windows-sdk-content
description: The DrawDibUpdate macro draws the last frame in the DrawDib off-screen buffer.
old-location: multimedia\drawdibupdate.htm
old-project: Multimedia
ms.assetid: 049a513a-bae1-4551-8700-cef417ed5373
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: DrawDibUpdate, DrawDibUpdate macro [Windows Multimedia], _win32_DrawDibUpdate, multimedia.drawdibupdate, vfw/DrawDibUpdate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - DrawDibUpdate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
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
 

 


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

# CopyCursor macro


## -description


Copies the specified cursor.


## -parameters




### -param pcur [in]

Type: <b>HCURSOR</b>

A handle to the cursor to be copied.


## -remarks



<b>CopyCursor</b> enables an application or DLL to obtain the handle to a cursor shape owned by another module. Then if the other module is freed, the application is still able to use the cursor shape. 

Before closing, an application must call the <a href="https://msdn.microsoft.com/fee6d837-9fc7-4ea6-b5d7-3889a64ccdea">DestroyCursor</a> function to free any system resources associated with the cursor. 

Do not use the <b>CopyCursor</b> function for animated cursors. Instead, use the <a href="https://msdn.microsoft.com/3912d9e3-f507-4046-80fd-12e76a61edc7">CopyImage</a> function.

<b>CopyCursor</b> is implemented as a call to the <a href="https://msdn.microsoft.com/69127d3a-de0d-4d76-8957-33ef4efed6d0">CopyIcon</a> function.

<pre class="syntax" xml:space="preserve"><code>#define CopyCursor(pcur) ((HCURSOR)CopyIcon((HICON)(pcur)))</code></pre>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/69127d3a-de0d-4d76-8957-33ef4efed6d0">CopyIcon</a>



<a href="https://msdn.microsoft.com/3912d9e3-f507-4046-80fd-12e76a61edc7">CopyImage</a>



<a href="https://msdn.microsoft.com/d24e21f2-224d-4f32-aa0b-70844e3628ad">Cursors</a>



<a href="https://msdn.microsoft.com/fee6d837-9fc7-4ea6-b5d7-3889a64ccdea">DestroyCursor</a>



<a href="https://msdn.microsoft.com/29ac39ae-244a-404c-9501-68c7992366a1">GetCursor</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/69bb9f90-5366-4141-97b6-57e41b774614">SetCursor</a>



<a href="https://msdn.microsoft.com/6712b6b7-bdb0-4078-ba38-7ad744bbf765">ShowCursor</a>
 

 


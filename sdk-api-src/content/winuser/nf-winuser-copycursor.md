---
UID: NF:winuser.CopyCursor
title: CopyCursor macro
author: windows-sdk-content
description: Copies the specified cursor.
old-location: menurc\copycursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\copycursor.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CopyCursor, CopyCursor function [Menus and Other Resources], _win32_CopyCursor, _win32_copycursor_cpp, menurc.copycursor, winui._win32_copycursor, winuser/CopyCursor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: winuser.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - CopyCursor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 


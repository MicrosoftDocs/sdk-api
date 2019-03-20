---
UID: NF:winuser.CopyCursor
title: CopyCursor macro (winuser.h)
author: windows-sdk-content
description: Copies the specified cursor.
old-location: menurc\copycursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\copycursor.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CopyCursor, CopyCursor function [Menus and Other Resources], _win32_CopyCursor, _win32_copycursor_cpp, menurc.copycursor, winui._win32_copycursor, winuser/CopyCursor
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

Before closing, an application must call the <a href="https://msdn.microsoft.com/en-us/library/ms648386(v=VS.85).aspx">DestroyCursor</a> function to free any system resources associated with the cursor. 

Do not use the <b>CopyCursor</b> function for animated cursors. Instead, use the <a href="https://msdn.microsoft.com/en-us/library/ms648031(v=VS.85).aspx">CopyImage</a> function.

<b>CopyCursor</b> is implemented as a call to the <a href="https://msdn.microsoft.com/en-us/library/ms648058(v=VS.85).aspx">CopyIcon</a> function.

<pre class="syntax" xml:space="preserve"><code>#define CopyCursor(pcur) ((HCURSOR)CopyIcon((HICON)(pcur)))</code></pre>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648058(v=VS.85).aspx">CopyIcon</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648031(v=VS.85).aspx">CopyImage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646970(v=VS.85).aspx">Cursors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648386(v=VS.85).aspx">DestroyCursor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648388(v=VS.85).aspx">GetCursor</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648393(v=VS.85).aspx">SetCursor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648396(v=VS.85).aspx">ShowCursor</a>
 

 


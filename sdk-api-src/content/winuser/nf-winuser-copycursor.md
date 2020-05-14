---
UID: NF:winuser.CopyCursor
title: CopyCursor macro (winuser.h)
description: Copies the specified cursor.helpviewer_keywords: ["CopyCursor","CopyCursor function [Menus and Other Resources]","_win32_CopyCursor","_win32_copycursor_cpp","menurc.copycursor","winui._win32_copycursor","winuser/CopyCursor"]
old-location: menurc\copycursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\copycursor.htm
ms.date: 12/05/2018
ms.keywords: CopyCursor, CopyCursor function [Menus and Other Resources], _win32_CopyCursor, _win32_copycursor_cpp, menurc.copycursor, winui._win32_copycursor, winuser/CopyCursor
f1_keywords:
- winuser/CopyCursor
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

Before closing, an application must call the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-destroycursor">DestroyCursor</a> function to free any system resources associated with the cursor. 

Do not use the <b>CopyCursor</b> function for animated cursors. Instead, use the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-copyimage">CopyImage</a> function.

<b>CopyCursor</b> is implemented as a call to the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-copyicon">CopyIcon</a> function.

<pre class="syntax" xml:space="preserve"><code>#define CopyCursor(pcur) ((HCURSOR)CopyIcon((HICON)(pcur)))</code></pre>



## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-copyicon">CopyIcon</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-copyimage">CopyImage</a>



<a href="https://docs.microsoft.com/windows/desktop/menurc/cursors">Cursors</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-destroycursor">DestroyCursor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getcursor">GetCursor</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setcursor">SetCursor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-showcursor">ShowCursor</a>
 

 


---
UID: NF:winuser.DestroyCursor
title: DestroyCursor function
author: windows-sdk-content
description: Destroys a cursor and frees any memory the cursor occupied. Do not use this function to destroy a shared cursor.
old-location: menurc\destroycursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\destroycursor.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: DestroyCursor, DestroyCursor function [Menus and Other Resources], _win32_DestroyCursor, _win32_destroycursor_cpp, menurc.destroycursor, winui._win32_destroycursor, winuser/DestroyCursor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-0.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - api-ms-win-ntuser-ie-gui-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-RTCore-NTUser-Cursor-L1-1-0.dll
 - MinUser.dll
api_name:
 - DestroyCursor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DestroyCursor function


## -description


Destroys a cursor and frees any memory the cursor occupied. Do not use this function to destroy a shared cursor.


## -parameters




### -param hCursor [in]

Type: <b>HCURSOR</b>

A handle to the cursor to be destroyed. The cursor must not be in use. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <b>DestroyCursor</b> function destroys a nonshared cursor. Do not use this function to destroy a shared cursor. A shared cursor is valid as long as the module from which it was loaded remains in memory. The following functions obtain a shared cursor: 

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms648391(v=VS.85).aspx">LoadCursor</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms648392(v=VS.85).aspx">LoadCursorFromFile</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms648045(v=VS.85).aspx">LoadImage</a> (if you use the <b>LR_SHARED</b> flag) </li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms648031(v=VS.85).aspx">CopyImage</a> (if you use the <b>LR_COPYRETURNORG</b> flag and the <i>hImage</i> parameter is a shared cursor) </li>
</ul>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648384(v=VS.85).aspx">CopyCursor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648031(v=VS.85).aspx">CopyImage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648385(v=VS.85).aspx">CreateCursor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646970(v=VS.85).aspx">Cursors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648391(v=VS.85).aspx">LoadCursor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648392(v=VS.85).aspx">LoadCursorFromFile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648045(v=VS.85).aspx">LoadImage</a>



<b>Reference</b>
 

 


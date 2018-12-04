---
UID: NF:winuser.DestroyCursor
title: DestroyCursor function
author: windows-sdk-content
description: Destroys a cursor and frees any memory the cursor occupied. Do not use this function to destroy a shared cursor.
old-location: menurc\destroycursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\destroycursor.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
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
<a href="https://msdn.microsoft.com/302f9238-4b03-4688-8b9b-a598beffb575">LoadCursor</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3b44be8d-5a68-4b0f-ba86-7a0decf01c5a">LoadCursorFromFile</a>
</li>
<li>
<a href="https://msdn.microsoft.com/27a18763-60e0-4a91-9262-807ea2b67416">LoadImage</a> (if you use the <b>LR_SHARED</b> flag) </li>
<li>
<a href="https://msdn.microsoft.com/3912d9e3-f507-4046-80fd-12e76a61edc7">CopyImage</a> (if you use the <b>LR_COPYRETURNORG</b> flag and the <i>hImage</i> parameter is a shared cursor) </li>
</ul>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/2ae1ee3e-5114-4712-a2a8-b413b83bb58c">CopyCursor</a>



<a href="https://msdn.microsoft.com/3912d9e3-f507-4046-80fd-12e76a61edc7">CopyImage</a>



<a href="https://msdn.microsoft.com/8a5bb069-4c2b-4924-9455-e6c91fef8461">CreateCursor</a>



<a href="https://msdn.microsoft.com/d24e21f2-224d-4f32-aa0b-70844e3628ad">Cursors</a>



<a href="https://msdn.microsoft.com/302f9238-4b03-4688-8b9b-a598beffb575">LoadCursor</a>



<a href="https://msdn.microsoft.com/3b44be8d-5a68-4b0f-ba86-7a0decf01c5a">LoadCursorFromFile</a>



<a href="https://msdn.microsoft.com/27a18763-60e0-4a91-9262-807ea2b67416">LoadImage</a>



<b>Reference</b>
 

 


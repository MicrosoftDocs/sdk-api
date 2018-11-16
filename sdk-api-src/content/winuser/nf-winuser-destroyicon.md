---
UID: NF:winuser.DestroyIcon
title: DestroyIcon function
author: windows-sdk-content
description: Destroys an icon and frees any memory the icon occupied.
old-location: menurc\destroyicon.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\destroyicon.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DestroyIcon, DestroyIcon function [Menus and Other Resources], _win32_DestroyIcon, _win32_destroyicon_cpp, menurc.destroyicon, winui._win32_destroyicon, winuser/DestroyIcon
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
 - Ext-MS-Win-NTUser-Gui-L1-3-0.dll
api_name:
 - DestroyIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DestroyIcon
: 
---

# DestroyIcon function


## -description


Destroys an icon and frees any memory the icon occupied. 


## -parameters




### -param hIcon [in]

Type: <b>HICON</b>

A handle to the icon to be destroyed. The icon must not be in use. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



It is only necessary to call <b>DestroyIcon</b> for icons and cursors created with the following functions: <a href="https://msdn.microsoft.com/ab53ad0c-1821-401c-be88-996dbe797e45">CreateIconFromResourceEx</a> (if called without the <b>LR_SHARED</b> flag), <a href="https://msdn.microsoft.com/adef864c-22f5-4d72-adc7-02d9b7a09e86">CreateIconIndirect</a>, and <a href="https://msdn.microsoft.com/69127d3a-de0d-4d76-8957-33ef4efed6d0">CopyIcon</a>. Do not use this function to destroy a shared icon. A shared icon is valid as long as the module from which it was loaded remains in memory. The following functions obtain a shared icon. 

<ul>
<li>
<a href="https://msdn.microsoft.com/3a8099f8-9db7-4ef8-838f-ca8f272df531">LoadIcon</a>
</li>
<li>
<a href="https://msdn.microsoft.com/27a18763-60e0-4a91-9262-807ea2b67416">LoadImage</a> (if you use the <b>LR_SHARED</b> flag) </li>
<li>
<a href="https://msdn.microsoft.com/3912d9e3-f507-4046-80fd-12e76a61edc7">CopyImage</a> (if you use the <b>LR_COPYRETURNORG</b> flag and the <i>hImage</i> parameter is a shared icon) </li>
<li>
<a href="https://msdn.microsoft.com/c5a1c301-0b1f-49b7-9648-9cf706b74e05">CreateIconFromResource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ab53ad0c-1821-401c-be88-996dbe797e45">CreateIconFromResourceEx</a> (if you use the <b>LR_SHARED</b> flag)
					</li>
</ul>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/69127d3a-de0d-4d76-8957-33ef4efed6d0">CopyIcon</a>



<a href="https://msdn.microsoft.com/c5a1c301-0b1f-49b7-9648-9cf706b74e05">CreateIconFromResource</a>



<a href="https://msdn.microsoft.com/ab53ad0c-1821-401c-be88-996dbe797e45">CreateIconFromResourceEx</a>



<a href="https://msdn.microsoft.com/adef864c-22f5-4d72-adc7-02d9b7a09e86">CreateIconIndirect</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<b>Reference</b>
 

 


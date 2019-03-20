---
UID: NF:winuser.DestroyIcon
title: DestroyIcon function (winuser.h)
author: windows-sdk-content
description: Destroys an icon and frees any memory the icon occupied.
old-location: menurc\destroyicon.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\destroyicon.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DestroyIcon, DestroyIcon function [Menus and Other Resources], _win32_DestroyIcon, _win32_destroyicon_cpp, menurc.destroyicon, winui._win32_destroyicon, winuser/DestroyIcon
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



It is only necessary to call <b>DestroyIcon</b> for icons and cursors created with the following functions: <a href="https://msdn.microsoft.com/en-us/library/ms648061(v=VS.85).aspx">CreateIconFromResourceEx</a> (if called without the <b>LR_SHARED</b> flag), <a href="https://msdn.microsoft.com/en-us/library/ms648062(v=VS.85).aspx">CreateIconIndirect</a>, and <a href="https://msdn.microsoft.com/en-us/library/ms648058(v=VS.85).aspx">CopyIcon</a>. Do not use this function to destroy a shared icon. A shared icon is valid as long as the module from which it was loaded remains in memory. The following functions obtain a shared icon. 

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms648072(v=VS.85).aspx">LoadIcon</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms648045(v=VS.85).aspx">LoadImage</a> (if you use the <b>LR_SHARED</b> flag) </li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms648031(v=VS.85).aspx">CopyImage</a> (if you use the <b>LR_COPYRETURNORG</b> flag and the <i>hImage</i> parameter is a shared icon) </li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms648060(v=VS.85).aspx">CreateIconFromResource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms648061(v=VS.85).aspx">CreateIconFromResourceEx</a> (if you use the <b>LR_SHARED</b> flag)
					</li>
</ul>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648058(v=VS.85).aspx">CopyIcon</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648060(v=VS.85).aspx">CreateIconFromResource</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648061(v=VS.85).aspx">CreateIconFromResourceEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648062(v=VS.85).aspx">CreateIconIndirect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646973(v=VS.85).aspx">Icons</a>



<b>Reference</b>
 

 


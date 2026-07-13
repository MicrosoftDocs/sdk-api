---
UID: NF:winuser.DestroyIcon
title: DestroyIcon function (winuser.h)
description: Destroys an icon and frees any memory the icon occupied.
helpviewer_keywords: ["DestroyIcon","DestroyIcon function [Menus and Other Resources]","_win32_DestroyIcon","_win32_destroyicon_cpp","menurc.destroyicon","winui._win32_destroyicon","winuser/DestroyIcon"]
old-location: menurc\destroyicon.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\destroyicon.htm
ms.date: 12/05/2018
ms.keywords: DestroyIcon, DestroyIcon function [Menus and Other Resources], _win32_DestroyIcon, _win32_destroyicon_cpp, menurc.destroyicon, winui._win32_destroyicon, winuser/DestroyIcon
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DestroyIcon
 - winuser/DestroyIcon
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-gui-l1-1-1.dll
 - ext-ms-win-ntuser-gui-l1-3-1.dll
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
req.apiset: ext-ms-win-ntuser-gui-l1-1-0 (introduced in Windows 8)
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

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

It is only necessary to call <b>DestroyIcon</b> for icons and cursors created with the following functions: <a href="/windows/desktop/api/winuser/nf-winuser-createiconfromresourceex">CreateIconFromResourceEx</a> (if called without the <b>LR_SHARED</b> flag), <a href="/windows/desktop/api/winuser/nf-winuser-createiconindirect">CreateIconIndirect</a>, and <a href="/windows/desktop/api/winuser/nf-winuser-copyicon">CopyIcon</a>. Do not use this function to destroy a shared icon. A shared icon is valid as long as the module from which it was loaded remains in memory. The following functions obtain a shared icon. 

<ul>
<li>
<a href="/windows/desktop/api/winuser/nf-winuser-loadicona">LoadIcon</a>
</li>
<li>
<a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a> (if you use the <b>LR_SHARED</b> flag) </li>
<li>
<a href="/windows/desktop/api/winuser/nf-winuser-copyimage">CopyImage</a> (if you use the <b>LR_COPYRETURNORG</b> flag and the <i>hImage</i> parameter is a shared icon) </li>
<li>
<a href="/windows/desktop/api/winuser/nf-winuser-createiconfromresource">CreateIconFromResource</a>
</li>
<li>
<a href="/windows/desktop/api/winuser/nf-winuser-createiconfromresourceex">CreateIconFromResourceEx</a> (if you use the <b>LR_SHARED</b> flag)
					</li>
</ul>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-copyicon">CopyIcon</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createiconfromresource">CreateIconFromResource</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createiconfromresourceex">CreateIconFromResourceEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createiconindirect">CreateIconIndirect</a>



<a href="/windows/desktop/menurc/icons">Icons</a>



<b>Reference</b>

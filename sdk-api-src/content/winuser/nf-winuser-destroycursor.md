---
UID: NF:winuser.DestroyCursor
title: DestroyCursor function (winuser.h)
description: Destroys a cursor and frees any memory the cursor occupied. Do not use this function to destroy a shared cursor.
helpviewer_keywords: ["DestroyCursor","DestroyCursor function [Menus and Other Resources]","_win32_DestroyCursor","_win32_destroycursor_cpp","menurc.destroycursor","winui._win32_destroycursor","winuser/DestroyCursor"]
old-location: menurc\destroycursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\destroycursor.htm
ms.date: 12/05/2018
ms.keywords: DestroyCursor, DestroyCursor function [Menus and Other Resources], _win32_DestroyCursor, _win32_destroycursor_cpp, menurc.destroycursor, winui._win32_destroycursor, winuser/DestroyCursor
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
 - DestroyCursor
 - winuser/DestroyCursor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-cursor-l1-1-1.dll
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

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>DestroyCursor</b> function destroys a nonshared cursor. Do not use this function to destroy a shared cursor. A shared cursor is valid as long as the module from which it was loaded remains in memory. The following functions obtain a shared cursor: 

<ul>
<li>
<a href="/windows/desktop/api/winuser/nf-winuser-loadcursora">LoadCursor</a>
</li>
<li>
<a href="/windows/desktop/api/winuser/nf-winuser-loadcursorfromfilea">LoadCursorFromFile</a>
</li>
<li>
<a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a> (if you use the <b>LR_SHARED</b> flag) </li>
<li>
<a href="/windows/desktop/api/winuser/nf-winuser-copyimage">CopyImage</a> (if you use the <b>LR_COPYRETURNORG</b> flag and the <i>hImage</i> parameter is a shared cursor) </li>
</ul>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-copycursor">CopyCursor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-copyimage">CopyImage</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createcursor">CreateCursor</a>



<a href="/windows/desktop/menurc/cursors">Cursors</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadcursora">LoadCursor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadcursorfromfilea">LoadCursorFromFile</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a>



<b>Reference</b>
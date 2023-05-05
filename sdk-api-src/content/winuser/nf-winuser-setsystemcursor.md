---
UID: NF:winuser.SetSystemCursor
title: SetSystemCursor function (winuser.h)
description: Enables an application to customize the system cursors. It replaces the contents of the system cursor specified by the id parameter with the contents of the cursor specified by the hcur parameter and then destroys hcur.
helpviewer_keywords: ["OCR_APPSTARTING","OCR_CROSS","OCR_HAND","OCR_HELP","OCR_IBEAM","OCR_NO","OCR_NORMAL","OCR_SIZEALL","OCR_SIZENESW","OCR_SIZENS","OCR_SIZENWSE","OCR_SIZEWE","OCR_UP","OCR_WAIT","SetSystemCursor","SetSystemCursor function [Menus and Other Resources]","_win32_SetSystemCursor","_win32_setsystemcursor_cpp","menurc.setsystemcursor","winui._win32_setsystemcursor","winuser/SetSystemCursor"]
old-location: menurc\setsystemcursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\setsystemcursor.htm
ms.date: 12/05/2018
ms.keywords: OCR_APPSTARTING, OCR_CROSS, OCR_HAND, OCR_HELP, OCR_IBEAM, OCR_NO, OCR_NORMAL, OCR_SIZEALL, OCR_SIZENESW, OCR_SIZENS, OCR_SIZENWSE, OCR_SIZEWE, OCR_UP, OCR_WAIT, SetSystemCursor, SetSystemCursor function [Menus and Other Resources], _win32_SetSystemCursor, _win32_setsystemcursor_cpp, menurc.setsystemcursor, winui._win32_setsystemcursor, winuser/SetSystemCursor
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
 - SetSystemCursor
 - winuser/SetSystemCursor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - SetSystemCursor
---

# SetSystemCursor function


## -description

Enables an application to customize the system cursors. It replaces the contents of the system cursor specified by the <i>id</i> parameter with the contents of the cursor specified by the <i>hcur</i> parameter and then destroys <i>hcur</i>.

## -parameters

### -param hcur [in]

Type: <b>HCURSOR</b>

A handle to the cursor. The function replaces the contents of the system cursor specified by <i>id</i> with the contents of the cursor handled by <i>hcur</i>.

The system destroys <i>hcur</i> by calling the <a href="/windows/desktop/api/winuser/nf-winuser-destroycursor">DestroyCursor</a> function. Therefore, <i>hcur</i> cannot be a cursor loaded using the <a href="/windows/desktop/api/winuser/nf-winuser-loadcursora">LoadCursor</a> function. To specify a cursor loaded from a resource, copy the cursor using the <a href="/windows/desktop/api/winuser/nf-winuser-copycursor">CopyCursor</a> function, then pass the copy to <b>SetSystemCursor</b>.

### -param id [in]

Type: <b>DWORD</b>

The system cursor to replace with the contents of <i>hcur</i>. This parameter can be one of the following values. 

| Value | Meaning |
|---|---|
| **OCR\_NORMAL**<br/>`32512` | Normal select | 
| **OCR\_IBEAM**<br/>`32513` | Text select | 
| **OCR\_WAIT**<br/>`32514` | Busy | 
| **OCR\_CROSS**<br/>`32515` | Precision select | 
| **OCR\_UP**<br/>`32516` | Alternate select | 
| **OCR\_SIZENWSE**<br/>`32642` | Diagonal resize 1 | 
| **OCR\_SIZENESW**<br/>`32643` | Diagonal resize 2 | 
| **OCR\_SIZEWE**<br/>`32644` | Horizontal resize | 
| **OCR\_SIZENS**<br/>`32645` | Vertical resize | 
| **OCR\_SIZEALL**<br/>`32646` | Move |  
| **OCR\_NO**<br/>`32648` | Unavailable | 
| **OCR\_HAND**<br/>`32649` | Link select | 
| **OCR\_APPSTARTING**<br/>`32650` | Working in background |

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

For an application to use any of the OCR_ constants, the constant <b>OEMRESOURCE</b> must be defined before the Windows.h header file is included.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/menurc/cursors">Cursors</a>



<a href="/windows/desktop/api/winuser/nf-winuser-destroycursor">DestroyCursor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadcursora">LoadCursor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadcursorfromfilea">LoadCursorFromFile</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setcursor">SetCursor</a>

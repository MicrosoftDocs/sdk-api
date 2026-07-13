---
UID: NS:winuser.tagCREATESTRUCTA
title: CREATESTRUCTA (winuser.h)
description: Defines the initialization parameters passed to the window procedure of an application. These members are identical to the parameters of the CreateWindowEx function. (ANSI)
helpviewer_keywords: ["*LPCREATESTRUCTA","CREATESTRUCT","CREATESTRUCT structure [Windows and Messages]","CREATESTRUCTA","CREATESTRUCTW","LPCREATESTRUCT","LPCREATESTRUCT structure pointer [Windows and Messages]","_win32_CREATESTRUCT_str","_win32_createstruct_str_cpp","winmsg.createstruct","winui._win32_createstruct_str","winuser/CREATESTRUCT","winuser/CREATESTRUCTA","winuser/CREATESTRUCTW","winuser/LPCREATESTRUCT"]
old-location: winmsg\createstruct.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\createstruct.htm
ms.date: 12/05/2018
ms.keywords: '*LPCREATESTRUCTA, CREATESTRUCT, CREATESTRUCT structure [Windows and Messages], CREATESTRUCTA, CREATESTRUCTW, LPCREATESTRUCT, LPCREATESTRUCT structure pointer [Windows and Messages], _win32_CREATESTRUCT_str, _win32_createstruct_str_cpp, winmsg.createstruct, winui._win32_createstruct_str, winuser/CREATESTRUCT, winuser/CREATESTRUCTA, winuser/CREATESTRUCTW, winuser/LPCREATESTRUCT'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CREATESTRUCTW (Unicode) and CREATESTRUCTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CREATESTRUCTA, *LPCREATESTRUCTA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCREATESTRUCTA
 - winuser/tagCREATESTRUCTA
 - LPCREATESTRUCTA
 - winuser/LPCREATESTRUCTA
 - CREATESTRUCTA
 - winuser/CREATESTRUCTA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - CREATESTRUCT
 - CREATESTRUCTA
 - CREATESTRUCTW
---

# CREATESTRUCTA structure


## -description

Defines the initialization parameters passed to the window procedure of an application. These members are identical to the parameters of the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> function.

## -struct-fields

### -field lpCreateParams

Type: <b>LPVOID</b>

Contains additional data which may be used to create the window. If the window is being created as a result of a call to the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a> or <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> function, this member contains the value of the <i>lpParam</i> parameter specified in the function call.

If the window being created is a MDI client window, this member contains a pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-clientcreatestruct">CLIENTCREATESTRUCT</a> structure. If the window being created is a MDI child window, this member contains a pointer to an <a href="/windows/desktop/api/winuser/ns-winuser-mdicreatestructa">MDICREATESTRUCT</a> structure.

 If the window is being created from a dialog template, this member is the address of a <b>SHORT</b> value that specifies the size, in bytes, of the window creation data. The value is immediately followed by the creation data. For more information, see the following Remarks section.

### -field hInstance

Type: <b>HINSTANCE</b>

A handle to the module that owns the new window.

### -field hMenu

Type: <b>HMENU</b>

A handle to the menu to be used by the new window.

### -field hwndParent

Type: <b>HWND</b>

A handle to the parent window, if the window is a child window. If the window is owned, this member identifies the owner window. If the window is not a child or owned window, this member is <b>NULL</b>.

### -field cy

Type: <b>int</b>

The height of the new window, in pixels.

### -field cx

Type: <b>int</b>

The width of the new window, in pixels.

### -field y

Type: <b>int</b>

The y-coordinate of the upper left corner of the new window. If the new window is a child window, coordinates are relative to the parent window. Otherwise, the coordinates are relative to the screen origin.

### -field x

Type: <b>int</b>

The x-coordinate of the upper left corner of the new window. If the new window is a child window, coordinates are relative to the parent window. Otherwise, the coordinates are relative to the screen origin.

### -field style

Type: <b>LONG</b>

The style for the new window. For a list of possible values, see <a href="/windows/desktop/winmsg/window-styles">Window Styles</a>.

### -field lpszName

Type: <b>LPCTSTR</b>

The name of the new window.

### -field lpszClass

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string or an atom that specifies the class name of the new window.

### -field dwExStyle

Type: <b>DWORD</b>

The extended window style for the new window. For a list of possible values, see  <a href="/windows/desktop/winmsg/extended-window-styles">Extended Window Styles</a>.

## -remarks

Because the <b>lpszClass</b> member can contain a pointer to a local (and thus inaccessible) atom, do not obtain the class name by using this member. Use the <a href="/windows/desktop/api/winuser/nf-winuser-getclassname">GetClassName</a> function instead.

 You should access the data represented by the <b>lpCreateParams</b> member using a pointer that has been declared using the <b>UNALIGNED</b> type, because the pointer may not be <b>DWORD</b> aligned. This is demonstrated in the following example:

                


```
typedef struct tagMyData 
{
    // Define creation data here. 
} MYDATA; 
 
typedef struct tagMyDlgData 
{ 
    SHORT   cbExtra; 
    MYDATA  myData; 
} MYDLGDATA, UNALIGNED *PMYDLGDATA; 
 
PMYDLGDATA pMyDlgdata = (PMYDLGDATA) (((LPCREATESTRUCT) lParam)->lpCreateParams);
```






> [!NOTE]
> The winuser.h header defines CREATESTRUCT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/winmsg/about-the-multiple-document-interface">About the Multiple Document Interface</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a>



<a href="/windows/desktop/api/winuser/ns-winuser-mdicreatestructa">MDICREATESTRUCT</a>



<b>Reference</b>



<a href="/windows/desktop/winmsg/windows">Windows</a>

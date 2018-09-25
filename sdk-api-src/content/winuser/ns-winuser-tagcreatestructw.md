---
UID: NS:winuser.tagCREATESTRUCTW
title: tagCREATESTRUCTW
author: windows-sdk-content
description: Defines the initialization parameters passed to the window procedure of an application. These members are identical to the parameters of the CreateWindowEx function.
old-location: winmsg\createstruct.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowstructures\createstruct.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPCREATESTRUCTW, CREATESTRUCT, CREATESTRUCT structure [Windows and Messages], CREATESTRUCTA, CREATESTRUCTW, LPCREATESTRUCT, LPCREATESTRUCT structure pointer [Windows and Messages], _win32_CREATESTRUCT_str, _win32_createstruct_str_cpp, tagCREATESTRUCTW, winmsg.createstruct, winui._win32_createstruct_str, winuser/CREATESTRUCT, winuser/CREATESTRUCTA, winuser/CREATESTRUCTW, winuser/LPCREATESTRUCT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: CREATESTRUCTW, *LPCREATESTRUCTW
req.redist: 
---

# tagCREATESTRUCTW structure


## -description


Defines the initialization parameters passed to the window procedure of an application. These members are identical to the parameters of the <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function.


## -struct-fields




### -field lpCreateParams

Type: <b>LPVOID</b>

Contains additional data which may be used to create the window. If the window is being created as a result of a call to the <a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a> or <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function, this member contains the value of the <i>lpParam</i> parameter specified in the function call.

If the window being created is a MDI client window, this member contains a pointer to a <a href="https://msdn.microsoft.com/795396d0-4d3b-4e55-b339-cf02cdfd9b46">CLIENTCREATESTRUCT</a> structure. If the window being created is a MDI child window, this member contains a pointer to an <a href="https://msdn.microsoft.com/aac21a17-4302-4174-9d72-15366d964094">MDICREATESTRUCT</a> structure.

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

The style for the new window. For a list of possible values, see <a href="https://msdn.microsoft.com/bfc146f1-bebd-4e68-a29e-a73ff3e8f35b">Window Styles</a>.


### -field lpszName

Type: <b>LPCTSTR</b>

The name of the new window. 


### -field lpszClass

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string or an atom that specifies the class name of the new window. 


### -field dwExStyle

Type: <b>DWORD</b>

The extended window style for the new window. For a list of possible values, see  <a href="https://msdn.microsoft.com/5830B16E-CD52-4a1a-A1BD-3AFE66BA5FDD">Extended Window Styles</a>.


## -remarks



Because the <b>lpszClass</b> member can contain a pointer to a local (and thus inaccessable) atom, do not obtain the class name by using this member. Use the <a href="https://msdn.microsoft.com/039dd7cd-07cf-4c8a-9287-365d54da2f43">GetClassName</a> function instead.

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





## -see-also




<a href="https://msdn.microsoft.com/35dff281-3b11-4954-85cf-a0f1c9ed346a">About the Multiple Document Interface</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a>



<a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a>



<a href="https://msdn.microsoft.com/aac21a17-4302-4174-9d72-15366d964094">MDICREATESTRUCT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 


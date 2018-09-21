---
UID: NF:winuser.CreateCaret
title: CreateCaret function
author: windows-sdk-content
description: Creates a new shape for the system caret and assigns ownership of the caret to the specified window. The caret shape can be a line, a block, or a bitmap.
old-location: menurc\createcaret.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\carets\caretreference\caretfunctions\createcaret.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateCaret, CreateCaret function [Menus and Other Resources], _win32_CreateCaret, _win32_createcaret_cpp, menurc.createcaret, winui._win32_createcaret, winuser/CreateCaret
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
 - Ext-MS-Win-NTUser-caret-l1-1-0.dll
 - api-ms-win-ntuser-ie-caret-l1-1-0.dll
 - ie_stubs.dll
api_name:
 - CreateCaret
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateCaret function


## -description


Creates a new shape for the system caret and assigns ownership of the caret to the specified window. The caret shape can be a line, a block, or a bitmap.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window that owns the caret. 


### -param hBitmap [in, optional]

Type: <b>HBITMAP</b>

A handle to the bitmap that defines the caret shape. If this parameter is <b>NULL</b>, the caret is solid. If this parameter is <code>(HBITMAP) 1</code>, the caret is gray. If this parameter is a bitmap handle, the caret is the specified bitmap. The bitmap handle must have been created by the <a href="https://msdn.microsoft.com/b52e1baf-6a81-44bc-a061-4d42e6f4ed64">CreateBitmap</a>, <a href="https://msdn.microsoft.com/e9a5b525-a6b6-4309-9e53-69d274b85783">CreateDIBitmap</a>, or <a href="https://msdn.microsoft.com/5eed5f78-deaf-4b23-986e-4802dc05936c">LoadBitmap</a> function.

If <i>hBitmap</i> is a bitmap handle, <b>CreateCaret</b> ignores the <i>nWidth</i> and <i>nHeight</i> parameters; the bitmap defines its own width and height.


### -param nWidth [in]

Type: <b>int</b>

The width of the caret, in logical units. If this parameter is zero, the width is set to the system-defined window border width. If <i>hBitmap</i> is a bitmap handle, <b>CreateCaret</b> ignores this parameter.


### -param nHeight [in]

Type: <b>int</b>

The height of the caret, in logical units. If this parameter is zero, the height is set to the system-defined window border height. If <i>hBitmap</i> is a bitmap handle, <b>CreateCaret</b> ignores this parameter. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.
                    

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <i>nWidth</i> and <i>nHeight</i> parameters specify the caret's width and height, in logical units; the exact width and height, in pixels, depend on the window's mapping mode. 

<b>CreateCaret</b> automatically destroys the previous caret shape, if any, regardless of the window that owns the caret. The caret is hidden until the application calls the <a href="https://msdn.microsoft.com/en-us/library/ms648406(v=VS.85).aspx">ShowCaret</a> function to make the caret visible. 

The system provides one caret per queue. A window should create a caret only when it has the keyboard focus or is active. The window should destroy the caret before losing the keyboard focus or becoming inactive. 

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The width and height parameters are interpreted as logical sizes in terms of the window in question. The calling thread is not taken into consideration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms646968(v=VS.85).aspx">Carets</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b52e1baf-6a81-44bc-a061-4d42e6f4ed64">CreateBitmap</a>



<a href="https://msdn.microsoft.com/e9a5b525-a6b6-4309-9e53-69d274b85783">CreateDIBitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648400(v=VS.85).aspx">DestroyCaret</a>



<a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648403(v=VS.85).aspx">HideCaret</a>



<a href="https://msdn.microsoft.com/5eed5f78-deaf-4b23-986e-4802dc05936c">LoadBitmap</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648406(v=VS.85).aspx">ShowCaret</a>
 

 


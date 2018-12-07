---
UID: NF:commctrl.CreateToolbarEx
title: CreateToolbarEx function
author: windows-sdk-content
description: Creates a toolbar window and adds the specified buttons to the toolbar.
old-location: controls\CreateToolbarEx.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\toolbar\functions\createtoolbarex.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateToolbarEx, CreateToolbarEx function [Windows Controls], _win32_CreateToolbarEx, _win32_CreateToolbarEx_cpp, commctrl/CreateToolbarEx, controls.CreateToolbarEx, controls._win32_CreateToolbarEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - CreateToolbarEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateToolbarEx function


## -description


Creates a toolbar window and adds the specified buttons to the toolbar. 
			
<div class="alert"><b>Note</b>   This function is deprecated, because it does not support all features of toolbars. Use <a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a> instead. For examples, see <a href="https://msdn.microsoft.com/en-us/library/Bb760446(v=VS.85).aspx">Using Toolbar Controls</a>.</div><div> </div>

## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to the parent window for the toolbar. 


### -param ws

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">DWORD</a></b>

Window styles for the toolbar. The <a href="https://msdn.microsoft.com/en-us/library/ms632600(v=VS.85).aspx">WS_CHILD</a> style is included by default. This parameter can also include a combination of styles as discussed in <a href="https://msdn.microsoft.com/en-us/library/Bb760439(v=VS.85).aspx">Toolbar Control and Button Styles</a>. 


### -param wID

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Control identifier for the toolbar. 


### -param nBitmaps

Type: <b>int</b>

Number of button images contained in the bitmap specified by 
					<i>hBMInst</i> and 
					<i>wBMID</i>.


### -param hBMInst

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HINSTANCE</a></b>

Module instance with the executable file that contains the bitmap resource. 


### -param wBMID

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT_PTR</a></b>

Resource identifier for the bitmap resource. If 
					<i>hBMInst</i> is <b>NULL</b>, this parameter must be a valid bitmap handle. 


### -param lpButtons

Type: <b>LPCTBBUTTON</b>

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/Bb760476(v=VS.85).aspx">TBBUTTON</a> structures that contain information about the buttons to add to the toolbar. 


### -param iNumButtons

Type: <b>int</b>

Number of buttons to add to the toolbar.


### -param dxButton

Type: <b>int</b>

Width, in pixels, of the buttons to add to the toolbar. 


### -param dyButton

Type: <b>int</b>

Height, in pixels, of the buttons to add to the toolbar. 


### -param dxBitmap

Type: <b>int</b>

Width, in pixels, of the button images to add to the buttons in the toolbar. 


### -param dyBitmap

Type: <b>int</b>

Height, in pixels, of the button images to add to the buttons in the toolbar. 


### -param uStructSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of a <a href="https://msdn.microsoft.com/en-us/library/Bb760476(v=VS.85).aspx">TBBUTTON</a> structure. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Returns the window handle to the toolbar if successful, or <b>NULL</b> otherwise. To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



Windows 95: The system can support a maximum of 16,364 window handles. 




---
UID: NF:commctrl.CreateToolbarEx
title: CreateToolbarEx function
author: windows-driver-content
description: Creates a toolbar window and adds the specified buttons to the toolbar.
old-location: controls\CreateToolbarEx.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\toolbar\functions\createtoolbarex.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
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
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Comctl32.dll
api_name:
-	CreateToolbarEx
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
---

# CreateToolbarEx function


## -description


Creates a toolbar window and adds the specified buttons to the toolbar. 
			
<div class="alert"><b>Note</b>   This function is deprecated, because it does not support all features of toolbars. Use <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> instead. For examples, see <a href="https://msdn.microsoft.com/5e52049c-58b4-478c-92ee-ea2f16534f6c">Using Toolbar Controls</a>.</div><div> </div>

## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the parent window for the toolbar. 


### -param ws

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Window styles for the toolbar. The <a href="https://msdn.microsoft.com/bfc146f1-bebd-4e68-a29e-a73ff3e8f35b">WS_CHILD</a> style is included by default. This parameter can also include a combination of styles as discussed in <a href="https://msdn.microsoft.com/75dc0c2c-6d1d-4b13-b0df-2cc541a9b1bb">Toolbar Control and Button Styles</a>. 


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

Pointer to an array of <a href="https://msdn.microsoft.com/c7dea982-d8b3-44e1-a4d2-3cca560c2096">TBBUTTON</a> structures that contain information about the buttons to add to the toolbar. 


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

Size of a <a href="https://msdn.microsoft.com/c7dea982-d8b3-44e1-a4d2-3cca560c2096">TBBUTTON</a> structure. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Returns the window handle to the toolbar if successful, or <b>NULL</b> otherwise. To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



Windows 95: The system can support a maximum of 16,364 window handles. 




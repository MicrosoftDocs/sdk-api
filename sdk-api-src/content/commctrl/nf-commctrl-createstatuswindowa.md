---
UID: NF:commctrl.CreateStatusWindowA
title: CreateStatusWindowA function
author: windows-sdk-content
description: Creates a status window, which is typically used to display the status of an application.
old-location: controls\CreateStatusWindow.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\status\functions\createstatuswindow.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CreateStatusWindow, CreateStatusWindow function [Windows Controls], CreateStatusWindowA, CreateStatusWindowW, _win32_CreateStatusWindow, _win32_CreateStatusWindow_cpp, commctrl/CreateStatusWindow, commctrl/CreateStatusWindowA, commctrl/CreateStatusWindowW, controls.CreateStatusWindow, controls._win32_CreateStatusWindow
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
req.unicode-ansi: CreateStatusWindowW (Unicode) and CreateStatusWindowA (ANSI)
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
 - CreateStatusWindow
 - CreateStatusWindowA
 - CreateStatusWindowW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateStatusWindowA function


## -description


Creates a status window, which is typically used to display the status of an application. The window generally appears at the bottom of the parent window, and it contains the specified text. 
			
<div class="alert"><b>Note</b>   This function is obsolete. Use <a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a> instead.</div><div> </div>

## -parameters




### -param style

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Window styles for the status window. This parameter must include the <a href="https://msdn.microsoft.com/bfc146f1-bebd-4e68-a29e-a73ff3e8f35b">WS_CHILD</a> style and should also include the <a href="https://msdn.microsoft.com/bfc146f1-bebd-4e68-a29e-a73ff3e8f35b">WS_VISIBLE</a> style. 


### -param lpszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

Pointer to a null-terminated string that specifies the status text for the first part. 


### -param hwndParent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

handle to the parent window. 


### -param wID

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Control identifier for the status window. The window procedure uses this value to identify messages it sends to the parent window. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Returns the handle to the status window if successful, or <b>NULL</b> otherwise. To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>CreateStatusWindow</b> function calls the <a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a> function to create the window. It passes the parameters to  without modification and sets the position, width, and height parameters to <b>CreateWindow</b>default values. 




---
UID: NF:commctrl.DefSubclassProc
title: DefSubclassProc function
author: windows-sdk-content
description: Calls the next handler in a window's subclass chain. The last handler in the subclass chain calls the original window procedure for the window.
old-location: shell\DefSubclassProc.htm
tech.root: shell
ms.assetid: 43b1efa5-11da-4a95-8d81-b0d8ae64733a
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: DefSubclassProc, DefSubclassProc function [Windows Shell], commctrl/DefSubclassProc, inet_DefSubclassProc, shell.DefSubclassProc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Comctl32.dll (version 5.8 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - DefSubclassProc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DefSubclassProc function


## -description


Calls the next handler in a window's subclass chain. The last handler in the subclass chain calls the original window procedure for the window.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window being subclassed.


### -param uMsg [in]

Type: <b>UINT</b>

A value of type unsigned <b>int</b> that specifies a window message.


### -param wParam [in]

Type: <b>WPARAM</b>

Specifies additional message information. The contents of this parameter depend on the value of the window message.


### -param lParam [in]

Type: <b>LPARAM</b>

Specifies additional message information. The contents of this parameter depend on the value of the window message. Note: On 64-bit versions of Windows LPARAM is a 64-bit value.


## -returns



Type: <b>LRESULT</b>

The returned value is specific to the message sent. This value should be ignored.




## -remarks



You do not need to call the default window procedure; this function calls it automatically.

The SUBCLASS module defines helper functions that are used to subclass windows. The code maintains a single property on the subclassed window and dispatches various subclass callbacks to its clients as required. The client is provided reference data and a default processing API.

A subclass callback is identified by a unique pairing of a callback function pointer and an unsigned ID value. Each callback can also store a single <b>DWORD</b> of reference data, which is passed to the callback function when it is called to filter messages. No reference counting is performed for the callback; it may repeatedly call <a href="https://msdn.microsoft.com/0b11144d-eb4e-462c-96d3-38c4bac48f2a">SetWindowSubclass</a> to alter the value of its reference data element.

<div class="alert"><b>Warning</b>  You cannot use the subclassing helper functions to subclass a window across threads.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/3969f18e-3e12-4770-8596-2c2c6519c2a7">GetWindowSubclass</a>



<a href="https://msdn.microsoft.com/09f27240-f3af-4791-afcb-a82bda79712a">RemoveWindowSubclass</a>



<a href="https://msdn.microsoft.com/0b11144d-eb4e-462c-96d3-38c4bac48f2a">SetWindowSubclass</a>
 

 


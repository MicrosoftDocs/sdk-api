---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SetDialogControlDpiChangeBehavior function


## -description


Overrides the default per-monitor DPI scaling behavior of a child window in a dialog.


## -parameters




### -param hWnd

TBD


### -param mask

A mask specifying the subset of flags to be changed.


### -param values

The desired value to be set for the specified subset of flags.


#### - hwnd

A handle for the window whose behavior will be modified.


## -returns



This function returns TRUE if the operation was successful, and FALSE otherwise. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

Possible errors are <b>ERROR_INVALID_HANDLE</b> if passed an invalid HWND, and <b>ERROR_ACCESS_DENIED</b> if the windows belongs to another process.




## -remarks



The behaviors are specified as values from the <a href="https://msdn.microsoft.com/B368D997-F409-491A-8578-004C7408A160">DIALOG_CONTROL_DPI_CHANGE_BEHAVIORS</a> enum. This function follows the typical two-parameter approach to setting flags, where a mask specifies the subset of the flags to be changed.

It is valid to set these behaviors on <i>any</i> window. It does not matter if the window is currently a child of a dialog at the point in time that SetDialogControlDpiChangeBehavior is called. The behaviors are retained and will take effect only when the window is an immediate child of a dialog that has per-monitor DPI scaling enabled.

This API influences individual controls within dialogs. The dialog-wide per-monitor DPI scaling behavior is controlled by <a href="https://msdn.microsoft.com/48A13F57-9D82-4F79-962B-FBD02FFF9B39">SetDialogDpiChangeBehavior</a>.




## -see-also




<a href="https://msdn.microsoft.com/B368D997-F409-491A-8578-004C7408A160">DIALOG_CONTROL_DPI_CHANGE_BEHAVIORS</a>



<a href="https://msdn.microsoft.com/1651353F-5823-41B8-AE52-016AEBA6C4F0">GetDialogControlDpiChangeBehavior</a>
 

 


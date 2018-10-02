---
UID: NF:winuser.SetDialogDpiChangeBehavior
title: SetDialogDpiChangeBehavior function
author: windows-sdk-content
description: Dialogs in Per-Monitor v2 contexts are automatically DPI scaled. This method lets you customize their DPI change behavior.
old-location: hidpi\setdialogdpichangebehavior.htm
tech.root: hidpi
ms.assetid: 48A13F57-9D82-4F79-962B-FBD02FFF9B39
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SetDialogDpiChangeBehavior, SetDialogDpiChangeBehavior function [High DPI], hidpi.setdialogdpichangebehavior, winuser/SetDialogDpiChangeBehavior
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
api_name:
 - SetDialogDpiChangeBehavior
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetDialogDpiChangeBehavior function


## -description


Dialogs in <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">Per-Monitor v2 contexts</a> are automatically DPI scaled. This method lets you customize their DPI change behavior.

This function works in conjunction with the <a href="https://msdn.microsoft.com/26248777-E95F-49BE-82D6-7237FAEE0627">DIALOG_DPI_CHANGE_BEHAVIORS</a> enum in order to override the default DPI scaling behavior for dialogs.  This function is called on a specified dialog, for which the specified flags are individually saved. 

This function does not affect the DPI scaling behavior for the child windows of the dialog in question - that is done with <a href="https://msdn.microsoft.com/52BB557B-0D70-4189-9BD0-EB94188EA4E7">SetDialogControlDpiChangeBehavior</a>.


## -parameters




### -param hDlg

A handle for the dialog whose behavior will be modified.


### -param mask

A mask specifying the subset of flags to be changed.


### -param values

The desired value to be set for the specified subset of flags.


## -returns



This function returns TRUE if the operation was successful, and FALSE otherwise. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

Possible errors are <b>ERROR_INVALID_HANDLE</b> if passed an invalid dialog HWND, and <b>ERROR_ACCESS_DENIED</b> if the dialog belongs to another process.




## -remarks



For extensibility, <a href="https://msdn.microsoft.com/26248777-E95F-49BE-82D6-7237FAEE0627">DIALOG_DPI_CHANGE_BEHAVIORS</a> was modeled as a set of bit-flags representing separate behaviors. This function follows the typical two-parameter approach to setting flags, where a mask specifies the subset of the flags to be changed.

It is not an error to call this API outside of Per Monitor v2 contexts, though the flags will have no effect on the behavior of the specified dialog until the context is changed to Per Monitor v2.




## -see-also




<a href="https://msdn.microsoft.com/26248777-E95F-49BE-82D6-7237FAEE0627">DIALOG_DPI_CHANGE_BEHAVIORS</a>



<a href="https://msdn.microsoft.com/8ED61C77-36C8-453B-BAB1-505CE4974D63">GetDialogDpiChangeBehavior</a>
 

 


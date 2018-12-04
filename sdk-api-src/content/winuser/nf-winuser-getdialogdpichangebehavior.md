---
UID: NF:winuser.GetDialogDpiChangeBehavior
title: GetDialogDpiChangeBehavior function
author: windows-sdk-content
description: Returns the flags that might have been set on a given dialog by an earlier call to SetDialogDpiChangeBehavior.
old-location: hidpi\getdialogdpichangebehavior.htm
tech.root: hidpi
ms.assetid: 8ED61C77-36C8-453B-BAB1-505CE4974D63
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetDialogDpiChangeBehavior, GetDialogDpiChangeBehavior function [High DPI], hidpi.getdialogdpichangebehavior, winuser/GetDialogDpiChangeBehavior
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
 - GetDialogDpiChangeBehavior
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetDialogDpiChangeBehavior function


## -description


Returns the flags that might have been set on a given dialog by an earlier call to <a href="https://msdn.microsoft.com/48A13F57-9D82-4F79-962B-FBD02FFF9B39">SetDialogDpiChangeBehavior</a>.

 If that function was never called on the dialog, the return value will be zero.


## -parameters




### -param hDlg

The handle for the dialog to examine.


## -returns



The flags set on the given dialog. If passed an invalid handle, this function will return zero, and set its <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">last error</a> to <b>ERROR_INVALID_HANDLE</b>.




## -remarks



It can be difficult to distinguish between a return value of <b>DDC_DEFAULT</b> and the error case, which is zero. To determine between the two, it is recommended that you call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError()</a> to check the error.




## -see-also




<a href="https://msdn.microsoft.com/26248777-E95F-49BE-82D6-7237FAEE0627">DIALOG_DPI_CHANGE_BEHAVIORS</a>



<a href="https://msdn.microsoft.com/48A13F57-9D82-4F79-962B-FBD02FFF9B39">SetDialogDpiChangeBehavior</a>
 

 


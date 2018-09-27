---
UID: NF:winuser.GetDialogControlDpiChangeBehavior
title: GetDialogControlDpiChangeBehavior function
author: windows-sdk-content
description: Retrieves and per-monitor DPI scaling behavior overrides of a child window in a dialog.
old-location: hidpi\getdialogresizebehavior.htm
tech.root: hidpi
ms.assetid: 1651353F-5823-41B8-AE52-016AEBA6C4F0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetDialogControlDpiChangeBehavior, GetDialogControlDpiChangeBehavior function [High DPI], hidpi.getdialogresizebehavior, winuser/GetDialogControlDpiChangeBehavior
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
 - GetDialogControlDpiChangeBehavior
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetDialogControlDpiChangeBehavior function


## -description


Retrieves and per-monitor DPI scaling behavior overrides of a child window in a dialog.


## -parameters




### -param hWnd

The handle for the window to examine.


## -returns



The flags set on the given window. If passed an invalid handle, this function will return zero, and set its <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">last error</a> to <b>ERROR_INVALID_HANDLE</b>.




## -see-also




<a href="https://msdn.microsoft.com/B368D997-F409-491A-8578-004C7408A160">DIALOG_CONTROL_DPI_CHANGE_BEHAVIORS</a>



<a href="https://msdn.microsoft.com/52BB557B-0D70-4189-9BD0-EB94188EA4E7">SetDialogControlDpiChangeBehavior</a>
 

 


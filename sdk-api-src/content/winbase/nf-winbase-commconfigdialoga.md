---
UID: NF:winbase.CommConfigDialogA
title: CommConfigDialogA function
author: windows-sdk-content
description: Displays a driver-supplied configuration dialog box.
old-location: base\commconfigdialog.htm
tech.root: devio
ms.assetid: 6c7a3833-1d40-40c5-bfa7-14523bc73ab0
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: CommConfigDialog, CommConfigDialog function, CommConfigDialogA, CommConfigDialogW, _win32_commconfigdialog, base.commconfigdialog, winbase/CommConfigDialog, winbase/CommConfigDialogA, winbase/CommConfigDialogW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CommConfigDialogW (Unicode) and CommConfigDialogA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - CommConfigDialog
 - CommConfigDialogA
 - CommConfigDialogW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CommConfigDialogA function


## -description


Displays a driver-supplied configuration dialog box.


## -parameters




### -param lpszName [in]

The name of the device for which a dialog box should be displayed. For example, COM1 through COM9 are serial ports and LPT1 through LPT9 are parallel ports.


### -param hWnd [in]

A handle to the window that owns the dialog box. This parameter can be any valid window handle, or it should be <b>NULL</b> if the dialog box is to have no owner.


### -param lpCC [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/9fd66f39-06a2-4159-9d1e-4ba84570c510">COMMCONFIG</a> structure. This structure contains initial settings for the dialog box before the call, and changed values after the call.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>CommConfigDialog</b> function requires a dynamic-link library (DLL) provided by the communications hardware vendor.




## -see-also




<a href="https://msdn.microsoft.com/9fd66f39-06a2-4159-9d1e-4ba84570c510">COMMCONFIG</a>



<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>
 

 


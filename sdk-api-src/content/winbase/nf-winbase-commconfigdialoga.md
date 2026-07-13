---
UID: NF:winbase.CommConfigDialogA
title: CommConfigDialogA function (winbase.h)
description: Displays a driver-supplied configuration dialog box. (ANSI)
helpviewer_keywords: ["CommConfigDialogA", "winbase/CommConfigDialogA"]
old-location: base\commconfigdialog.htm
tech.root: base
ms.assetid: 6c7a3833-1d40-40c5-bfa7-14523bc73ab0
ms.date: 12/05/2018
ms.keywords: CommConfigDialog, CommConfigDialog function, CommConfigDialogA, CommConfigDialogW, _win32_commconfigdialog, base.commconfigdialog, winbase/CommConfigDialog, winbase/CommConfigDialogA, winbase/CommConfigDialogW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CommConfigDialogA
 - winbase/CommConfigDialogA
dev_langs:
 - c++
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
<a href="/windows/desktop/api/winbase/ns-winbase-commconfig">COMMCONFIG</a> structure. This structure contains initial settings for the dialog box before the call, and changed values after the call.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>CommConfigDialog</b> function requires a dynamic-link library (DLL) provided by the communications hardware vendor.





> [!NOTE]
> The winbase.h header defines CommConfigDialog as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-commconfig">COMMCONFIG</a>



<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>

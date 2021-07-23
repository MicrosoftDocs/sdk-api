---
UID: NF:shlobj_core.IProgressDialog.Timer
title: IProgressDialog::Timer (shlobj_core.h)
description: Resets the progress dialog box timer to zero.
helpviewer_keywords: ["IProgressDialog interface [Windows Shell]","Timer method","IProgressDialog.Timer","IProgressDialog::Timer","PDTIMER_PAUSE","PDTIMER_RESET","PDTIMER_RESUME","Timer","Timer method [Windows Shell]","Timer method [Windows Shell]","IProgressDialog interface","_win32_IProgressDialog_Timer","shell.IProgressDialog_Timer","shlobj_core/IProgressDialog::Timer"]
old-location: shell\IProgressDialog_Timer.htm
tech.root: shell
ms.assetid: ab048787-e555-4d5d-994a-1fc6f273312b
ms.date: 12/05/2018
ms.keywords: IProgressDialog interface [Windows Shell],Timer method, IProgressDialog.Timer, IProgressDialog::Timer, PDTIMER_PAUSE, PDTIMER_RESET, PDTIMER_RESUME, Timer, Timer method [Windows Shell], Timer method [Windows Shell],IProgressDialog interface, _win32_IProgressDialog_Timer, shell.IProgressDialog_Timer, shlobj_core/IProgressDialog::Timer
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IProgressDialog::Timer
 - shlobj_core/IProgressDialog::Timer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IProgressDialog.Timer
---

# IProgressDialog::Timer


## -description

Resets the progress dialog box timer to zero.

## -parameters

### -param dwTimerAction [in]

Type: <b>DWORD</b>

Flags that indicate the action to be taken by the timer. One of the following values:



#### PDTIMER_RESET

Resets the timer to zero. Progress will be calculated from the time this method is called.



#### PDTIMER_PAUSE

Progress has been suspended.



#### PDTIMER_RESUME

Progress has been resumed.

### -param pvResevered

Type: <b>LPCVOID</b>

Reserved. Set to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The timer is used to estimate the remaining time. It is started when your application calls <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iprogressdialog-startprogressdialog">IProgressDialog::StartProgressDialog</a>. Unless your application will start immediately, it should call <b>Timer</b> just before starting the operation. This practice ensures that the time estimates will be as accurate as possible. This method should not be called after the first call to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iprogressdialog-setprogress">IProgressDialog::SetProgress</a>.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iprogressdialog">IProgressDialog</a>
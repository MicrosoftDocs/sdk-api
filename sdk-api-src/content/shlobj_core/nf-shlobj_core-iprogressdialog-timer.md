---
UID: NF:shlobj_core.IProgressDialog.Timer
title: IProgressDialog::Timer
author: windows-sdk-content
description: Resets the progress dialog box timer to zero.
old-location: shell\IProgressDialog_Timer.htm
tech.root: shell
ms.assetid: ab048787-e555-4d5d-994a-1fc6f273312b
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: IProgressDialog interface [Windows Shell],Timer method, IProgressDialog.Timer, IProgressDialog::Timer, PDTIMER_PAUSE, PDTIMER_RESET, PDTIMER_RESUME, Timer, Timer method [Windows Shell], Timer method [Windows Shell],IProgressDialog interface, _win32_IProgressDialog_Timer, shell.IProgressDialog_Timer, shlobj_core/IProgressDialog::Timer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IProgressDialog.Timer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

TBD




#### - pvReserved

Type: <b>LPCVOID</b>

Reserved. Set to <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The timer is used to estimate the remaining time. It is started when your application calls <a href="https://msdn.microsoft.com/0cafe878-c95f-416e-8291-51d9a5a17a71">IProgressDialog::StartProgressDialog</a>. Unless your application will start immediately, it should call <b>Timer</b> just before starting the operation. This practice ensures that the time estimates will be as accurate as possible. This method should not be called after the first call to <a href="https://msdn.microsoft.com/50df7b32-e345-4379-809f-6870b53417b8">IProgressDialog::SetProgress</a>.




## -see-also




<a href="https://msdn.microsoft.com/ba0fb1f9-f67f-4cc7-96d8-4c4ccdd213eb">IProgressDialog</a>
 

 


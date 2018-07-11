---
UID: NF:winnls32.WINNLSEnableIME
title: WINNLSEnableIME function
author: windows-sdk-content
description: Temporarily enables or disables an Input Method Editor (IME) and, at the same time, turns on or off the display of all windows owned by the IME.
old-location: winprog\_win32_winnlsenableime.htm
old-project: DevNotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\winnlsenableime.htm
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: WINNLSEnableIME, WINNLSEnableIME function [Windows API], _win32_WINNLSEnableIME, winnls32/WINNLSEnableIME, winprog._win32_winnlsenableime, winui._win32_winnlsenableime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnls32.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NUMBERFMTW, *LPNUMBERFMTW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - WINNLSEnableIME
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WINNLSEnableIME function


## -description


Temporarily enables or disables an Input Method Editor (IME) and, at the same time, turns on or off the display of all windows owned by the IME.
        
            
<div class="alert"><b>Note</b>  This function is obsolete and should not be used.</div><div> </div>

## -parameters




### -param HWND

TBD


### -param BOOL

TBD




#### - bFlag [in]

<b>TRUE</b> to enable the IME; <b>FALSE</b> to disable.


#### - hwnd [in]

Must be <b>NULL</b>. Specifying a particular IME for each application is not supported.


## -returns



The previous state of the IME. <b>TRUE</b> if it was enabled before this call, otherwise, <b>FALSE</b>.




## -remarks



The terms "enabled" and "disabled" in regard to this function are defined as follows:
            
                

If an IME is disabled, <a href="https://msdn.microsoft.com/library/Aa969466(v=VS.85).aspx">IME_WINDOWUPDATE(FALSE)</a> is issued to the IME, which responds by deleting the conversion and system windows. With the IME disabled, keyboard messages are not sent to the IME, but are sent directly to the application. Even if the IME is disabled, the API that uses the <a href="https://msdn.microsoft.com/library/Aa969468(v=VS.85).aspx">SendIMEMessageEx</a> function is still valid.

If an IME is enabled, <a href="https://msdn.microsoft.com/library/Aa969466(v=VS.85).aspx">IME_WINDOWUPDATE(TRUE)</a> is issued to the IME, which responds by redisplaying the conversion and system windows. With the IME enabled, keyboard messages are sent to the IME.




---
UID: NF:winnls32.WINNLSEnableIME
title: WINNLSEnableIME function (winnls32.h)
description: Temporarily enables or disables an Input Method Editor (IME) and, at the same time, turns on or off the display of all windows owned by the IME.
helpviewer_keywords: ["WINNLSEnableIME","WINNLSEnableIME function [Windows API]","_win32_WINNLSEnableIME","winnls32/WINNLSEnableIME","winprog._win32_winnlsenableime","winui._win32_winnlsenableime"]
old-location: winprog\_win32_winnlsenableime.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\winnlsenableime.htm
ms.date: 12/05/2018
ms.keywords: WINNLSEnableIME, WINNLSEnableIME function [Windows API], _win32_WINNLSEnableIME, winnls32/WINNLSEnableIME, winprog._win32_winnlsenableime, winui._win32_winnlsenableime
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WINNLSEnableIME
 - winnls32/WINNLSEnableIME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - WINNLSEnableIME
---

# WINNLSEnableIME function


## -description

Temporarily enables or disables an Input Method Editor (IME) and, at the same time, turns on or off the display of all windows owned by the IME.
        
            
<div class="alert"><b>Note</b>  This function is obsolete and should not be used.</div><div> </div>

## -parameters

### -param HWND [in]

Must be <b>NULL</b>. Specifying a particular IME for each application is not supported.

### -param BOOL [in]

<b>TRUE</b> to enable the IME; <b>FALSE</b> to disable.

## -returns

The previous state of the IME. <b>TRUE</b> if it was enabled before this call, otherwise, <b>FALSE</b>.

## -remarks

The terms "enabled" and "disabled" in regard to this function are defined as follows:
            
                

If an IME is disabled, <a href="/windows/desktop/api/ime/ns-ime-imestruct">IME_WINDOWUPDATE(FALSE)</a> is issued to the IME, which responds by deleting the conversion and system windows. With the IME disabled, keyboard messages are not sent to the IME, but are sent directly to the application. Even if the IME is disabled, the API that uses the <a href="/windows/desktop/api/ime/nf-ime-sendimemessageexa">SendIMEMessageEx</a> function is still valid.

If an IME is enabled, <a href="/windows/desktop/api/ime/ns-ime-imestruct">IME_WINDOWUPDATE(TRUE)</a> is issued to the IME, which responds by redisplaying the conversion and system windows. With the IME enabled, keyboard messages are sent to the IME.
---
UID: NF:winuser.InitializeTouchInjection
title: InitializeTouchInjection function (winuser.h)
description: Configures the touch injection context for the calling application and initializes the maximum number of simultaneous contacts that the app can inject.
helpviewer_keywords: ["InitializeTouchInjection","InitializeTouchInjection function [Windows Touch]","input_touchinjection.initializetouchinjection","touch_injection.initializetouchinjection","winuser/InitializeTouchInjection"]
old-location: input_touchinjection\initializetouchinjection.htm
tech.root: controls
ms.assetid: 79cc2a05-d8ee-4d87-9c7b-fa7d5354b04f
ms.date: 12/05/2018
ms.keywords: InitializeTouchInjection, InitializeTouchInjection function [Windows Touch], input_touchinjection.initializetouchinjection, touch_injection.initializetouchinjection, winuser/InitializeTouchInjection
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - InitializeTouchInjection
 - winuser/InitializeTouchInjection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-wmpointermin-l1-1-0.dll
 - api-ms-win-rtcore-ntuser-wmpointer-l1-2-0.dll
 - user32.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-0.dll
 - MinUser.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-1.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - InitializeTouchInjection
req.apiset: ext-ms-win-rtcore-ntuser-wmpointer-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# InitializeTouchInjection function


## -description

Configures the touch injection context for the calling application and initializes the maximum number of simultaneous contacts that the app can inject.<div class="alert"><b>Note</b>  <b>InitializeTouchInjection</b> must precede any call to  <a href="/windows/desktop/api/winuser/nf-winuser-injecttouchinput">InjectTouchInput</a>.</div>
<div> </div>

## -parameters

### -param maxCount [in]

The maximum number of touch contacts. 

The <i>maxCount</i> parameter must be greater than 0 and less than or equal to MAX_TOUCH_COUNT (256) as  defined in winuser.h.

### -param dwMode [in]

The contact visualization mode. 

The <i>dwMode</i> parameter must be   <a href="/previous-versions/windows/desktop/input_touchinjection/constants">TOUCH_FEEDBACK_DEFAULT</a>, <b>TOUCH_FEEDBACK_INDIRECT</b>, or <b>TOUCH_FEEDBACK_NONE</b>.

## -returns

If the function succeeds, the return value is TRUE.

If the function fails, the return value is FALSE. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If <a href="/previous-versions/windows/desktop/input_touchinjection/constants">TOUCH_FEEDBACK_DEFAULT</a> is set, the injected touch feedback may get suppressed by the end-user settings in the <b>Pen and Touch</b> control panel. 

If <a href="/previous-versions/windows/desktop/input_touchinjection/constants">TOUCH_FEEDBACK_INDIRECT</a> is set, the injected touch feedback overrides the end-user settings in the <b>Pen and Touch</b> control panel. 

If <a href="/previous-versions/windows/desktop/input_touchinjection/constants">TOUCH_FEEDBACK_INDIRECT</a> or <b>TOUCH_FEEDBACK_NONE</b> are set,  touch feedback provided by applications and controls may not be affected.

## -see-also

<a href="/previous-versions/windows/desktop/input_touchinjection/functions">Functions</a>

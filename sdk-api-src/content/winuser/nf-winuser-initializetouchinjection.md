---
UID: NF:winuser.InitializeTouchInjection
title: InitializeTouchInjection function
author: windows-sdk-content
description: Configures the touch injection context for the calling application and initializes the maximum number of simultaneous contacts that the app can inject.
old-location: input_touchinjection\initializetouchinjection.htm
tech.root: Input_TouchInjection
ms.assetid: 79cc2a05-d8ee-4d87-9c7b-fa7d5354b04f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: InitializeTouchInjection, InitializeTouchInjection function [Windows Touch], input_touchinjection.initializetouchinjection, touch_injection.initializetouchinjection, winuser/InitializeTouchInjection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-0.dll
 - MinUser.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-l1-1-1.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - InitializeTouchInjection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InitializeTouchInjection function


## -description


Configures the touch injection context for the calling application and initializes the maximum number of simultaneous contacts that the app can inject.<div class="alert"><b>Note</b>  <b>InitializeTouchInjection</b> must precede any call to  <a href="https://msdn.microsoft.com/c3c1425e-2af6-4ecb-a0b2-a456654f7a53">InjectTouchInput</a>.</div>
<div> </div>



## -parameters




### -param maxCount [in]

The maximum number of touch contacts. 

The <i>maxCount</i> parameter must be greater than 0 and less than or equal to MAX_TOUCH_COUNT (256) as  defined in winuser.h.


### -param dwMode [in]

The contact visualization mode. 

The <i>dwMode</i> parameter must be   <a href="https://msdn.microsoft.com/52941DF1-88AF-452B-BF3E-838ADBDBC9B2">TOUCH_FEEDBACK_DEFAULT</a>, <b>TOUCH_FEEDBACK_INDIRECT</b>, or <b>TOUCH_FEEDBACK_NONE</b>.


## -returns



If the function succeeds, the return value is TRUE.

If the function fails, the return value is FALSE. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If <a href="https://msdn.microsoft.com/52941DF1-88AF-452B-BF3E-838ADBDBC9B2">TOUCH_FEEDBACK_DEFAULT</a> is set, the injected touch feedback may get suppressed by the end-user settings in the <b>Pen and Touch</b> control panel. 

If <a href="https://msdn.microsoft.com/52941DF1-88AF-452B-BF3E-838ADBDBC9B2">TOUCH_FEEDBACK_INDIRECT</a> is set, the injected touch feedback overrides the end-user settings in the <b>Pen and Touch</b> control panel. 

If <a href="https://msdn.microsoft.com/52941DF1-88AF-452B-BF3E-838ADBDBC9B2">TOUCH_FEEDBACK_INDIRECT</a> or <b>TOUCH_FEEDBACK_NONE</b> are set,  touch feedback provided by applications and controls may not be affected.




## -see-also




<a href="https://msdn.microsoft.com/8C2DF633-EACB-4B99-91D9-BCB7BE518A2E">Functions</a>
 

 


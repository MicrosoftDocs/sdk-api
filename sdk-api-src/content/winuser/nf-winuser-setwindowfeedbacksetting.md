---
UID: NF:winuser.SetWindowFeedbackSetting
title: SetWindowFeedbackSetting function (winuser.h)
author: windows-sdk-content
description: Sets the feedback configuration for a window.
old-location: input_feedback\setwindowfeedbacksetting.htm
tech.root: Input_Feedback
ms.assetid: 72bee160-7004-40be-9c91-e431b06ccaed
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetWindowFeedbackSetting, SetWindowFeedbackSetting function, input_feedback.setwindowfeedbacksetting, inputfeedbackui.setwindowfeedbacksetting, winuser/SetWindowFeedbackSetting
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
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - MinUser.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - SetWindowFeedbackSetting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetWindowFeedbackSetting function


## -description


Sets the feedback configuration for a window.


## -parameters




### -param hwnd [in]

The window to configure feedback on.


### -param feedback [in]

One of the values from the <a href="https://msdn.microsoft.com/EEA3024E-D38C-4F4D-A63C-58ECB2B87F20">FEEDBACK_TYPE</a> enumeration.


### -param dwFlags [in]

Reserved. Must be 0.


### -param size [in]

The size, in bytes, of the configuration data. Must be sizeof(BOOL) or 0 if the feedback setting is being reset.


### -param configuration [in, optional]

The configuration data. Must be BOOL or NULL if the feedback setting is being reset.


## -returns



Returns TRUE if successful; otherwise, returns FALSE.




## -see-also




<a href="https://msdn.microsoft.com/9CC3EA75-8FD5-4A29-8FD7-785E25ACCBA2">Functions</a>



<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>
 

 


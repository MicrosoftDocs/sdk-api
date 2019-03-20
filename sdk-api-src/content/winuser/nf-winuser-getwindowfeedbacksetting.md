---
UID: NF:winuser.GetWindowFeedbackSetting
title: GetWindowFeedbackSetting function (winuser.h)
author: windows-sdk-content
description: Retrieves the feedback configuration for a window.
old-location: input_feedback\getwindowfeedbacksetting.htm
tech.root: Input_Feedback
ms.assetid: a40806b3-9085-42b6-9a87-95be0d1669c6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetWindowFeedbackSetting, GetWindowFeedbackSetting function, input_feedback.getwindowfeedbacksetting, inputfeedbackui.getwindowfeedbacksetting, winuser/GetWindowFeedbackSetting
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
 - GetWindowFeedbackSetting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetWindowFeedbackSetting function


## -description


Retrieves the feedback configuration for a window.


## -parameters




### -param hwnd [in]

The window to check for feedback configuration.


### -param feedback [in]

One of the values from the <a href="https://msdn.microsoft.com/EEA3024E-D38C-4F4D-A63C-58ECB2B87F20">FEEDBACK_TYPE</a> enumeration.


### -param dwFlags [in]

Specify <a href="https://msdn.microsoft.com/1B0EA599-6618-4DF2-B8C7-91A534BD85C0">GWFS_INCLUDE_ANCESTORS</a> to check the parent window chain until a value is found. The default is 0 and indicates that only the specified window will be checked.


### -param pSize [in, out]

The size of memory region that the <i>config</i> parameter points to. 

The <i>pSize</i> parameter specifies the size of the configuration data for the feedback type in <i>feedback</i> and must be sizeof(BOOL).


### -param config [out, optional]

The configuration data.

The <i>config</i> parameter must point to a value of type BOOL.


## -returns



Returns TRUE if the specified feedback setting is configured on the specified window. Otherwise, it returns FALSE (and <i>config</i> won't be modified).




## -see-also




<a href="https://msdn.microsoft.com/9CC3EA75-8FD5-4A29-8FD7-785E25ACCBA2">Functions</a>



<a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>
 

 


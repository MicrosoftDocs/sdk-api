---
UID: NF:winuser.SetWindowFeedbackSetting
title: SetWindowFeedbackSetting function (winuser.h)
description: Sets the feedback configuration for a window.
helpviewer_keywords: ["SetWindowFeedbackSetting","SetWindowFeedbackSetting function","input_feedback.setwindowfeedbacksetting","inputfeedbackui.setwindowfeedbacksetting","winuser/SetWindowFeedbackSetting"]
old-location: input_feedback\setwindowfeedbacksetting.htm
tech.root: controls
ms.assetid: 72bee160-7004-40be-9c91-e431b06ccaed
ms.date: 12/05/2018
ms.keywords: SetWindowFeedbackSetting, SetWindowFeedbackSetting function, input_feedback.setwindowfeedbacksetting, inputfeedbackui.setwindowfeedbacksetting, winuser/SetWindowFeedbackSetting
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
 - SetWindowFeedbackSetting
 - winuser/SetWindowFeedbackSetting
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
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - API-Ms-Win-RTCore-NTUser-WMPointer-L1-1-2.dll
 - MinUser.dll
 - API-MS-Win-RTCore-NTUser-WMPointer-L1-1-3.dll
api_name:
 - SetWindowFeedbackSetting
---

# SetWindowFeedbackSetting function


## -description

Sets the feedback configuration for a window.

## -parameters

### -param hwnd [in]

The window to configure feedback on.

### -param feedback [in]

One of the values from the <a href="/windows/desktop/api/winuser/ne-winuser-feedback_type">FEEDBACK_TYPE</a> enumeration.

### -param dwFlags [in]

Reserved. Must be 0.

### -param size [in]

The size, in bytes, of the configuration data. Must be sizeof(BOOL) or 0 if the feedback setting is being reset.

### -param configuration [in, optional]

The configuration data. Must be BOOL or NULL if the feedback setting is being reset.

## -returns

Returns TRUE if successful; otherwise, returns FALSE.

## -see-also

<a href="/previous-versions/windows/desktop/input_feedback/functions">Functions</a>



<a href="/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>
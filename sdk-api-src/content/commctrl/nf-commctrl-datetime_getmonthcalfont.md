---
UID: NF:commctrl.DateTime_GetMonthCalFont
title: DateTime_GetMonthCalFont macro (commctrl.h)
description: Gets the font that the date and time picker (DTP) control's child month calendar control is currently using. You can use this macro or send the DTM_GETMCFONT message explicitly.
helpviewer_keywords: ["DateTime_GetMonthCalFont","DateTime_GetMonthCalFont macro [Windows Controls]","_win32_DateTime_GetMonthCalFont","_win32_DateTime_GetMonthCalFont_cpp","commctrl/DateTime_GetMonthCalFont","controls.DateTime_GetMonthCalFont","controls._win32_DateTime_GetMonthCalFont"]
old-location: controls\DateTime_GetMonthCalFont.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_getmonthcalfont.htm
ms.date: 10/21/2024
ms.keywords: DateTime_GetMonthCalFont, DateTime_GetMonthCalFont macro [Windows Controls], _win32_DateTime_GetMonthCalFont, _win32_DateTime_GetMonthCalFont_cpp, commctrl/DateTime_GetMonthCalFont, controls.DateTime_GetMonthCalFont, controls._win32_DateTime_GetMonthCalFont
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DateTime_GetMonthCalFont
 - commctrl/DateTime_GetMonthCalFont
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - DateTime_GetMonthCalFont
---

# DateTime_GetMonthCalFont macro

## -syntax

```cpp
HFONT DateTime_GetMonthCalFont(
   HWND hdp
);
```

## -returns

Type: **[HFONT](/windows/desktop/winprog/windows-data-types)**

Returns an HFONT value that is the handle to the current font.


## -description

Gets the font that the date and time picker (DTP) control's child month calendar control is currently using. You can use this macro or send the <a href="/windows/desktop/Controls/dtm-getmcfont">DTM_GETMCFONT</a> message explicitly.

## -parameters

### -param hdp

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a DTP control.

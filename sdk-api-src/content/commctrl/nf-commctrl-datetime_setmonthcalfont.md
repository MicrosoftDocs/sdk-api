---
UID: NF:commctrl.DateTime_SetMonthCalFont
title: DateTime_SetMonthCalFont macro (commctrl.h)
description: Sets the font to be used by the date and time picker (DTP) control's child month calendar control. You can use this macro or explicitly send the DTM_SETMCFONT message.
helpviewer_keywords: ["DateTime_SetMonthCalFont","DateTime_SetMonthCalFont macro [Windows Controls]","_win32_DateTime_SetMonthCalFont","_win32_DateTime_SetMonthCalFont_cpp","commctrl/DateTime_SetMonthCalFont","controls.DateTime_SetMonthCalFont","controls._win32_DateTime_SetMonthCalFont"]
old-location: controls\DateTime_SetMonthCalFont.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_setmonthcalfont.htm
ms.date: 12/05/2018
ms.keywords: DateTime_SetMonthCalFont, DateTime_SetMonthCalFont macro [Windows Controls], _win32_DateTime_SetMonthCalFont, _win32_DateTime_SetMonthCalFont_cpp, commctrl/DateTime_SetMonthCalFont, controls.DateTime_SetMonthCalFont, controls._win32_DateTime_SetMonthCalFont
f1_keywords:
- commctrl/DateTime_SetMonthCalFont
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Commctrl.h
api_name:
- DateTime_SetMonthCalFont
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DateTime_SetMonthCalFont macro


## -description


Sets the font to be used by the date and time picker (DTP) control's child month calendar control. You can use this macro or explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Controls/dtm-setmcfont">DTM_SETMCFONT</a> message. 


## -parameters




### -param hdp

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a DTP control. 


### -param hfont

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HFONT</a></b>

A handle to the font that will be set. 


### -param fRedraw

Type: <b>long</b>

Specifies whether the control should be redrawn immediately upon setting the font. Setting this parameter to <b>TRUE</b> causes the control to redraw itself. 


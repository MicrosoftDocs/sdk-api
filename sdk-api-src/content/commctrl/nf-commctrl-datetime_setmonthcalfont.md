---
UID: NF:commctrl.DateTime_SetMonthCalFont
title: DateTime_SetMonthCalFont macro
author: windows-sdk-content
description: Sets the font to be used by the date and time picker (DTP) control's child month calendar control. You can use this macro or explicitly send the DTM_SETMCFONT message.
old-location: controls\DateTime_SetMonthCalFont.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_setmonthcalfont.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DateTime_SetMonthCalFont, DateTime_SetMonthCalFont macro [Windows Controls], _win32_DateTime_SetMonthCalFont, _win32_DateTime_SetMonthCalFont_cpp, commctrl/DateTime_SetMonthCalFont, controls.DateTime_SetMonthCalFont, controls._win32_DateTime_SetMonthCalFont
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DateTime_SetMonthCalFont macro


## -description


Sets the font to be used by the date and time picker (DTP) control's child month calendar control. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/5033e975-9b68-438a-99c3-80ca02cd59e7">DTM_SETMCFONT</a> message. 


## -parameters




### -param hdp

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a DTP control. 


### -param hfont

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HFONT</a></b>

A handle to the font that will be set. 


### -param fRedraw

Type: <b>long</b>

Specifies whether the control should be redrawn immediately upon setting the font. Setting this parameter to <b>TRUE</b> causes the control to redraw itself. 


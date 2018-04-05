---
UID: NF:commctrl.DateTime_SetMonthCalStyle
title: DateTime_SetMonthCalStyle macro
author: windows-driver-content
description: Sets the style for a specified date and time picker (DTP) control. Use this macro or send the DTM_SETMCSTYLE message explicitly.
old-location: controls\DateTime_SetMonthCalStyle.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_setmonthcalstyle.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: DateTime_SetMonthCalStyle, DateTime_SetMonthCalStyle macro [Windows Controls], _shell_DateTime_SetMonthCalStyle, _shell_DateTime_SetMonthCalStyle_cpp, commctrl/DateTime_SetMonthCalStyle, controls.DateTime_SetMonthCalStyle, controls._shell_DateTime_SetMonthCalStyle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	DateTime_SetMonthCalStyle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DateTime_SetMonthCalStyle macro


## -description


Sets the style for a specified date and time picker (DTP) control. Use this macro or send the <a href="https://msdn.microsoft.com/6b480a1e-c76e-4026-ab2a-5ec53df6fa28">DTM_SETMCSTYLE</a> message explicitly.


## -parameters




### -param hdp [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the DTP.


### -param dwStyle [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

<a href="https://msdn.microsoft.com/8d9b2239-fd13-4579-81a2-0385fd318e83">Month Calendar Control Styles</a>

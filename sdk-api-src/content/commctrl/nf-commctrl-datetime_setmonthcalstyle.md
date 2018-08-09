---
UID: NF:commctrl.DateTime_SetMonthCalStyle
title: DateTime_SetMonthCalStyle macro
author: windows-sdk-content
description: Sets the style for a specified date and time picker (DTP) control. Use this macro or send the DTM_SETMCSTYLE message explicitly.
old-location: controls\DateTime_SetMonthCalStyle.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_setmonthcalstyle.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DateTime_SetMonthCalStyle, DateTime_SetMonthCalStyle macro [Windows Controls], _shell_DateTime_SetMonthCalStyle, _shell_DateTime_SetMonthCalStyle_cpp, commctrl/DateTime_SetMonthCalStyle, controls.DateTime_SetMonthCalStyle, controls._shell_DateTime_SetMonthCalStyle
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - DateTime_SetMonthCalStyle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DateTime_SetMonthCalStyle macro


## -description


Sets the style for a specified date and time picker (DTP) control. Use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761778(v=VS.85).aspx">DTM_SETMCSTYLE</a> message explicitly.


## -parameters




### -param hdp [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the DTP.


### -param dwStyle [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

<a href="https://msdn.microsoft.com/en-us/library/Bb760919(v=VS.85).aspx">Month Calendar Control Styles</a>

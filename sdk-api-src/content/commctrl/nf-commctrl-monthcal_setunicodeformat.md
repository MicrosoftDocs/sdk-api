---
UID: NF:commctrl.MonthCal_SetUnicodeFormat
title: MonthCal_SetUnicodeFormat macro
author: windows-sdk-content
description: Sets the Unicode character format flag for the control.
old-location: controls\MonthCal_SetUnicodeFormat.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setunicodeformat.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: MonthCal_SetUnicodeFormat, MonthCal_SetUnicodeFormat macro [Windows Controls], _win32_MonthCal_SetUnicodeFormat, _win32_MonthCal_SetUnicodeFormat_cpp, commctrl/MonthCal_SetUnicodeFormat, controls.MonthCal_SetUnicodeFormat, controls._win32_MonthCal_SetUnicodeFormat
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
 - MonthCal_SetUnicodeFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MonthCal_SetUnicodeFormat macro


## -description


Sets the Unicode character format flag for the control. This message allows you to change the character set used by the control at run time rather than having to re-create the control. You can use this macro or send the <a href="https://msdn.microsoft.com/250789b5-694b-4502-9cc0-3bc260ea06e7">MCM_SETUNICODEFORMAT</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the control. 


### -param fUnicode

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Determines the character set that is used by the control. If this value is nonzero, the control will use Unicode characters. If this value is zero, the control will use ANSI characters. 


## -see-also




<a href="https://msdn.microsoft.com/c6206fdb-9c3d-4331-89f6-ed6e38aeb935">MonthCal_GetUnicodeFormat</a>
 

 


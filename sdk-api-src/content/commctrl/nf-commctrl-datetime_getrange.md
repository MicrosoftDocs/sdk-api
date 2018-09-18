---
UID: NF:commctrl.DateTime_GetRange
title: DateTime_GetRange macro
author: windows-sdk-content
description: Gets the current minimum and maximum allowable system times for a date and time picker (DTP) control. You can use this macro, or send the DTM_GETRANGE message explicitly.
old-location: controls\DateTime_GetRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_getrange.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: DateTime_GetRange, DateTime_GetRange macro [Windows Controls], _win32_DateTime_GetRange, _win32_DateTime_GetRange_cpp, commctrl/DateTime_GetRange, controls.DateTime_GetRange, controls._win32_DateTime_GetRange
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
 - DateTime_GetRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DateTime_GetRange macro


## -description


Gets the current minimum and maximum allowable system times for a date and time picker (DTP) control. You can use this macro, or send the <a href="https://msdn.microsoft.com/190cada6-49ee-483f-a464-d3d789127159">DTM_GETRANGE</a> message explicitly. 


## -parameters




### -param hdp

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a DTP control.


### -param rgst

Type: <b>LPSYSTEMTIME</b>

A pointer to a two-element array of <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structures. 


## -remarks



The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range. If the <a href="https://msdn.microsoft.com/9ac12f31-09d8-4220-939c-24fbb92cb6ed">DateTime_SetSystemtime</a> message specifies a date and time that falls outside the range, it will fail.




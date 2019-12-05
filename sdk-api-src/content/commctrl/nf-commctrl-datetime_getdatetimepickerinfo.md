---
UID: NF:commctrl.DateTime_GetDateTimePickerInfo
title: DateTime_GetDateTimePickerInfo macro (commctrl.h)
description: Gets information for a specified date and time picker (DTP) control.
old-location: controls\DateTime_GetDateTimePickerInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_getdatetimepickerinfo.htm
ms.date: 12/05/2018
ms.keywords: DateTime_GetDateTimePickerInfo, DateTime_GetDateTimePickerInfo macro [Windows Controls], _shell_DateTime_GetDateTimePickerInfo, _shell_DateTime_GetDateTimePickerInfo_cpp, commctrl/DateTime_GetDateTimePickerInfo, controls.DateTime_GetDateTimePickerInfo, controls._shell_DateTime_GetDateTimePickerInfo
ms.topic: macro
f1_keywords:
- commctrl/DateTime_GetDateTimePickerInfo
dev_langs:
- c++
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
- DateTime_GetDateTimePickerInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DateTime_GetDateTimePickerInfo macro


## -description


Gets information for a specified date and time picker (DTP) control.


## -parameters




### -param hdp [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the DTP control.


### -param pdtpi [in, out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-datetimepickerinfo">DATETIMEPICKERINFO</a>*</b>

<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-datetimepickerinfo">DATETIMEPICKERINFO</a>
<b>cbSize</b>

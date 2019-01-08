---
UID: NF:commctrl.DateTime_GetDateTimePickerInfo
title: DateTime_GetDateTimePickerInfo macro
author: windows-sdk-content
description: Gets information for a specified date and time picker (DTP) control.
old-location: controls\DateTime_GetDateTimePickerInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_getdatetimepickerinfo.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DateTime_GetDateTimePickerInfo, DateTime_GetDateTimePickerInfo macro [Windows Controls], _shell_DateTime_GetDateTimePickerInfo, _shell_DateTime_GetDateTimePickerInfo_cpp, commctrl/DateTime_GetDateTimePickerInfo, controls.DateTime_GetDateTimePickerInfo, controls._shell_DateTime_GetDateTimePickerInfo
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DateTime_GetDateTimePickerInfo macro


## -description


Gets information for a specified date and time picker (DTP) control.


## -parameters




### -param hdp [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the DTP control.


### -param pdtpi [in, out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb761729(v=VS.85).aspx">DATETIMEPICKERINFO</a>*</b>

<a href="https://msdn.microsoft.com/en-us/library/Bb761729(v=VS.85).aspx">DATETIMEPICKERINFO</a>
<b>cbSize</b>

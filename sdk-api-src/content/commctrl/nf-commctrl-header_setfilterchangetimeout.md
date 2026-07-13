---
UID: NF:commctrl.Header_SetFilterChangeTimeout
title: Header_SetFilterChangeTimeout macro (commctrl.h)
description: Sets the timeout interval between the time a change takes place in the filter attributes and the posting of an HDN_FILTERCHANGE notification. You can use this macro or send the HDM_SETFILTERCHANGETIMEOUT message explicitly.
helpviewer_keywords: ["Header_SetFilterChangeTimeout","Header_SetFilterChangeTimeout macro [Windows Controls]","_win32_Header_SetFilterChangeTimeout","_win32_Header_SetFilterChangeTimeout_cpp","commctrl/Header_SetFilterChangeTimeout","controls.Header_SetFilterChangeTimeout","controls._win32_Header_SetFilterChangeTimeout"]
old-location: controls\Header_SetFilterChangeTimeout.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_setfilterchangetimeout.htm
ms.date: 10/21/2024
ms.keywords: Header_SetFilterChangeTimeout, Header_SetFilterChangeTimeout macro [Windows Controls], _win32_Header_SetFilterChangeTimeout, _win32_Header_SetFilterChangeTimeout_cpp, commctrl/Header_SetFilterChangeTimeout, controls.Header_SetFilterChangeTimeout, controls._win32_Header_SetFilterChangeTimeout
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
 - Header_SetFilterChangeTimeout
 - commctrl/Header_SetFilterChangeTimeout
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
 - Header_SetFilterChangeTimeout
---

# Header_SetFilterChangeTimeout macro

## -syntax

```cpp
int Header_SetFilterChangeTimeout(
   HWND hwnd,
   int  i
);
```

## -returns

Type: **int**

Returns the index of the filter control being modified.


## -description

Sets the timeout interval between the time a change takes place in the filter attributes and the posting of an <a href="/windows/desktop/Controls/hdn-filterchange">HDN_FILTERCHANGE</a> notification. You can use this macro or send the <a href="/windows/desktop/Controls/hdm-setfilterchangetimeout">HDM_SETFILTERCHANGETIMEOUT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the header control.

### -param i

Type: <b>int</b>

The timeout value, in milliseconds.

## -see-also

<a href="/windows/desktop/Controls/hdm-setfilterchangetimeout">HDM_SETFILTERCHANGETIMEOUT</a>



<a href="/windows/desktop/Controls/hdn-filterchange">HDN_FILTERCHANGE</a>



<b>Reference</b>

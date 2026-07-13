---
UID: NF:commctrl.Header_ClearAllFilters
title: Header_ClearAllFilters macro (commctrl.h)
description: Clears all of the filters for a given header control. You can use this macro or send the HDM_CLEARFILTER message explicitly.
helpviewer_keywords: ["Header_ClearAllFilters","Header_ClearAllFilters macro [Windows Controls]","_win32_Header_ClearAllFilters","_win32_Header_ClearAllFilters_cpp","commctrl/Header_ClearAllFilters","controls.Header_ClearAllFilters","controls._win32_Header_ClearAllFilters"]
old-location: controls\Header_ClearAllFilters.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\header\macros\header_clearallfilters.htm
ms.date: 10/21/2024
ms.keywords: Header_ClearAllFilters, Header_ClearAllFilters macro [Windows Controls], _win32_Header_ClearAllFilters, _win32_Header_ClearAllFilters_cpp, commctrl/Header_ClearAllFilters, controls.Header_ClearAllFilters, controls._win32_Header_ClearAllFilters
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
 - Header_ClearAllFilters
 - commctrl/Header_ClearAllFilters
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
 - Header_ClearAllFilters
---

# Header_ClearAllFilters macro

## -syntax

```cpp
int Header_ClearAllFilters(
   HWND hwnd
);
```

## -returns

Type: **int**

Returns an integer that indicates <b>TRUE</b>(1) or <b>FALSE</b>(0).


## -description

Clears all of the filters for a given header control. You can use this macro or send the <a href="/windows/desktop/Controls/hdm-clearfilter">HDM_CLEARFILTER</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the header control.

## -remarks

When all the filters are cleared, the <a href="/windows/desktop/Controls/hdn-filterchange">HDN_FILTERCHANGE</a> notification will be sent only once.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-header_clearfilter">Header_ClearFilter</a>

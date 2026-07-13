---
UID: NF:commctrl.MAKEIPRANGE
title: MAKEIPRANGE macro (commctrl.h)
description: Packs two byte-values into a single LPARAM suitable for use with the IPM_SETRANGE message.
helpviewer_keywords: ["MAKEIPRANGE","MAKEIPRANGE macro [Windows Controls]","_win32_MAKEIPRANGE","_win32_MAKEIPRANGE_cpp","commctrl/MAKEIPRANGE","controls.MAKEIPRANGE","controls._win32_MAKEIPRANGE"]
old-location: controls\MAKEIPRANGE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\ipaddress\macros\makeiprange.htm
ms.date: 10/21/2024
ms.keywords: MAKEIPRANGE, MAKEIPRANGE macro [Windows Controls], _win32_MAKEIPRANGE, _win32_MAKEIPRANGE_cpp, commctrl/MAKEIPRANGE, controls.MAKEIPRANGE, controls._win32_MAKEIPRANGE
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
 - MAKEIPRANGE
 - commctrl/MAKEIPRANGE
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
 - MAKEIPRANGE
---

# MAKEIPRANGE macro

## -syntax

```cpp
LPARAM MAKEIPRANGE(
   BYTE low,
   BYTE high
);
```

## -returns

Type: **[LPARAM](/windows/desktop/winprog/windows-data-types)**

Returns an LPARAM value that contains the range.


## -description

Packs two byte-values into a single LPARAM suitable for use with the <a href="/windows/desktop/Controls/ipm-setrange">IPM_SETRANGE</a> message.

## -parameters

### -param low

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The lower limit of the range.

### -param high

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The upper limit of the range.

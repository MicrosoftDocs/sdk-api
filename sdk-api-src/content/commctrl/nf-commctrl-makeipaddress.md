---
UID: NF:commctrl.MAKEIPADDRESS
title: MAKEIPADDRESS macro (commctrl.h)
description: Packs four byte-values into a single LPARAM suitable for use with the IPM_SETADDRESS message.
helpviewer_keywords: ["MAKEIPADDRESS","MAKEIPADDRESS macro [Windows Controls]","_win32_MAKEIPADDRESS","_win32_MAKEIPADDRESS_cpp","commctrl/MAKEIPADDRESS","controls.MAKEIPADDRESS","controls._win32_MAKEIPADDRESS"]
old-location: controls\MAKEIPADDRESS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\ipaddress\macros\makeipaddress.htm
ms.date: 10/21/2024
ms.keywords: MAKEIPADDRESS, MAKEIPADDRESS macro [Windows Controls], _win32_MAKEIPADDRESS, _win32_MAKEIPADDRESS_cpp, commctrl/MAKEIPADDRESS, controls.MAKEIPADDRESS, controls._win32_MAKEIPADDRESS
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
 - MAKEIPADDRESS
 - commctrl/MAKEIPADDRESS
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
 - MAKEIPADDRESS
---

# MAKEIPADDRESS macro

## -syntax

```cpp
LPARAM MAKEIPADDRESS(
   BYTE b1,
   BYTE b2,
   BYTE b3,
   BYTE b4
);
```

## -returns

Type: **[LPARAM](/windows/desktop/winprog/windows-data-types)**

Returns an LPARAM value that contains the address.


## -description

Packs four byte-values into a single LPARAM suitable for use with the <a href="/windows/desktop/Controls/ipm-setaddress">IPM_SETADDRESS</a> message.

## -parameters

### -param b1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The field 0 address.

### -param b2

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The field 1 address.

### -param b3

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The field 2 address.

### -param b4

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The field 3 address.

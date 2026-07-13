---
UID: NF:commctrl.THIRD_IPADDRESS
title: THIRD_IPADDRESS macro (commctrl.h)
description: Extracts the field 2 value from a packed IP address retrieved with the IPM_GETADDRESS message.
helpviewer_keywords: ["THIRD_IPADDRESS","THIRD_IPADDRESS macro [Windows Controls]","_win32_THIRD_IPADDRESS","_win32_THIRD_IPADDRESS_cpp","commctrl/THIRD_IPADDRESS","controls.THIRD_IPADDRESS","controls._win32_THIRD_IPADDRESS"]
old-location: controls\THIRD_IPADDRESS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\ipaddress\macros\third_ipaddress.htm
ms.date: 10/21/2024
ms.keywords: THIRD_IPADDRESS, THIRD_IPADDRESS macro [Windows Controls], _win32_THIRD_IPADDRESS, _win32_THIRD_IPADDRESS_cpp, commctrl/THIRD_IPADDRESS, controls.THIRD_IPADDRESS, controls._win32_THIRD_IPADDRESS
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
 - THIRD_IPADDRESS
 - commctrl/THIRD_IPADDRESS
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
 - THIRD_IPADDRESS
---

# THIRD_IPADDRESS macro

## -syntax

```cpp
BYTE THIRD_IPADDRESS(
   LPARAM x
);
```

## -returns

Type: **[BYTE](/windows/desktop/winprog/windows-data-types)**

Returns a BYTE value that contains the field 2 value.


## -description

Extracts the field 2 value from a packed IP address retrieved with the <a href="/windows/desktop/Controls/ipm-getaddress">IPM_GETADDRESS</a> message.

## -parameters

### -param x

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The packed IP address value.

---
UID: NF:commctrl.SECOND_IPADDRESS
title: SECOND_IPADDRESS macro (commctrl.h)
description: Extracts the field 1 value from a packed IP address retrieved with the IPM_GETADDRESS message.
helpviewer_keywords: ["SECOND_IPADDRESS","SECOND_IPADDRESS macro [Windows Controls]","_win32_SECOND_IPADDRESS","_win32_SECOND_IPADDRESS_cpp","commctrl/SECOND_IPADDRESS","controls.SECOND_IPADDRESS","controls._win32_SECOND_IPADDRESS"]
old-location: controls\SECOND_IPADDRESS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\ipaddress\macros\second_ipaddress.htm
ms.date: 10/21/2024
ms.keywords: SECOND_IPADDRESS, SECOND_IPADDRESS macro [Windows Controls], _win32_SECOND_IPADDRESS, _win32_SECOND_IPADDRESS_cpp, commctrl/SECOND_IPADDRESS, controls.SECOND_IPADDRESS, controls._win32_SECOND_IPADDRESS
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
 - SECOND_IPADDRESS
 - commctrl/SECOND_IPADDRESS
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
 - SECOND_IPADDRESS
---

# SECOND_IPADDRESS macro

## -syntax

```cpp
BYTE SECOND_IPADDRESS(
   LPARAM x
);
```

## -returns

Type: **[BYTE](/windows/desktop/winprog/windows-data-types)**

Returns a BYTE value that contains the field 1 value.


## -description

Extracts the field 1 value from a packed IP address retrieved with the <a href="/windows/desktop/Controls/ipm-getaddress">IPM_GETADDRESS</a> message.

## -parameters

### -param x

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The packed IP address value.

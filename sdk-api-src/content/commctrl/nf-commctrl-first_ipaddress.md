---
UID: NF:commctrl.FIRST_IPADDRESS
title: FIRST_IPADDRESS macro (commctrl.h)
description: Extracts the field 0 value from a packed IP address retrieved with the IPM_GETADDRESS message.
helpviewer_keywords: ["FIRST_IPADDRESS","FIRST_IPADDRESS macro [Windows Controls]","_win32_FIRST_IPADDRESS","_win32_FIRST_IPADDRESS_cpp","commctrl/FIRST_IPADDRESS","controls.FIRST_IPADDRESS","controls._win32_FIRST_IPADDRESS"]
old-location: controls\FIRST_IPADDRESS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\ipaddress\macros\first_ipaddress.htm
ms.date: 10/21/2024
ms.keywords: FIRST_IPADDRESS, FIRST_IPADDRESS macro [Windows Controls], _win32_FIRST_IPADDRESS, _win32_FIRST_IPADDRESS_cpp, commctrl/FIRST_IPADDRESS, controls.FIRST_IPADDRESS, controls._win32_FIRST_IPADDRESS
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
 - FIRST_IPADDRESS
 - commctrl/FIRST_IPADDRESS
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
 - FIRST_IPADDRESS
---

# FIRST_IPADDRESS macro

## -syntax

```cpp
BYTE FIRST_IPADDRESS(
   LPARAM x
);
```

## -returns

Type: **[BYTE](/windows/desktop/winprog/windows-data-types)**

Returns a <b>BYTE</b> value that contains the field 0 value.


## -description

Extracts the field 0 value from a packed IP address retrieved with the <a href="/windows/desktop/Controls/ipm-getaddress">IPM_GETADDRESS</a> message.

## -parameters

### -param x

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The packed IP address value.

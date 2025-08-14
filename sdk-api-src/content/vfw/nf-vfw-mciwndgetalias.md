---
UID: NF:vfw.MCIWndGetAlias
title: MCIWndGetAlias macro (vfw.h)
description: The MCIWndGetAlias macro retrieves the alias used to open an MCI device or file with the mciSendString function. You can use this macro or explicitly send the MCIWNDM_GETALIAS message.
helpviewer_keywords: ["MCIWndGetAlias","MCIWndGetAlias macro [Windows Multimedia]","_win32_MCIWndGetAlias","multimedia.mciwndgetalias","vfw/MCIWndGetAlias"]
old-location: multimedia\mciwndgetalias.htm
tech.root: Multimedia
ms.assetid: 24756da8-9d80-408b-81c5-34e6d3388838
ms.date: 07/01/2025
ms.keywords: MCIWndGetAlias, MCIWndGetAlias macro [Windows Multimedia], _win32_MCIWndGetAlias, multimedia.mciwndgetalias, vfw/MCIWndGetAlias
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - MCIWndGetAlias
 - vfw/MCIWndGetAlias
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - MCIWndGetAlias
---

# MCIWndGetAlias macro

## -syntax

```cpp
UINT MCIWndGetAlias(
     hwnd
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns the device alias.


## -description

The <b>MCIWndGetAlias</b> macro retrieves the alias used to open an MCI device or file with the <a href="/previous-versions/dd757161(v=vs.85)">mciSendString</a> function. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-getalias">MCIWNDM_GETALIAS</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-getalias">MCIWNDM_GETALIAS</a>

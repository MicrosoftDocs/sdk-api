---
UID: NF:vfw.MCIWndGetDeviceID
title: MCIWndGetDeviceID macro (vfw.h)
description: The MCIWndGetDeviceID macro retrieves the identifier of the current MCI device to use with the mciSendCommand function. You can use this macro or explicitly send the MCIWNDM_GETDEVICEID message.
helpviewer_keywords: ["MCIWndGetDeviceID","MCIWndGetDeviceID macro [Windows Multimedia]","_win32_MCIWndGetDeviceID","multimedia.mciwndgetdeviceid","vfw/MCIWndGetDeviceID"]
old-location: multimedia\mciwndgetdeviceid.htm
tech.root: Multimedia
ms.assetid: 07477a6a-fe75-47b6-9771-c3a649523e2a
ms.date: 07/01/2025
ms.keywords: MCIWndGetDeviceID, MCIWndGetDeviceID macro [Windows Multimedia], _win32_MCIWndGetDeviceID, multimedia.mciwndgetdeviceid, vfw/MCIWndGetDeviceID
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
 - MCIWndGetDeviceID
 - vfw/MCIWndGetDeviceID
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
 - MCIWndGetDeviceID
---

# MCIWndGetDeviceID macro

## -syntax

```cpp
UINT MCIWndGetDeviceID(
     hwnd
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns the device identifier.


## -description

The <b>MCIWndGetDeviceID</b> macro retrieves the identifier of the current MCI device to use with the <a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a> function. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-getdeviceid">MCIWNDM_GETDEVICEID</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/desktop/Multimedia/mciwndm-getdeviceid">MCIWNDM_GETDEVICEID</a>



<a href="/previous-versions/dd757160(v=vs.85)">mciSendCommand</a>

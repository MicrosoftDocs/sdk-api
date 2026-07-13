---
UID: NF:vfw.MCIWndSendString
title: MCIWndSendString macro (vfw.h)
description: The MCIWndSendString macro sends an MCI command in string form to the device associated with the MCIWnd window. You can use this macro or explicitly send the MCIWNDM_SENDSTRING message.
helpviewer_keywords: ["MCIWndSendString","MCIWndSendString macro [Windows Multimedia]","_win32_MCIWndSendString","multimedia.mciwndsendstring","vfw/MCIWndSendString"]
old-location: multimedia\mciwndsendstring.htm
tech.root: Multimedia
ms.assetid: d73b087b-c697-470b-aa19-ca14d18ac430
ms.date: 07/01/2025
ms.keywords: MCIWndSendString, MCIWndSendString macro [Windows Multimedia], _win32_MCIWndSendString, multimedia.mciwndsendstring, vfw/MCIWndSendString
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
 - MCIWndSendString
 - vfw/MCIWndSendString
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
 - MCIWndSendString
---

# MCIWndSendString macro

## -syntax

```cpp
LONG MCIWndSendString(
     hwnd,
     sz
);
```

## -returns

Type: **LONG**

Returns zero if successful or an error otherwise.


## -description

The <b>MCIWndSendString</b> macro sends an MCI command in string form to the device associated with the MCIWnd window. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-sendstring">MCIWNDM_SENDSTRING</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param sz

String command to send to the MCI device.

## -remarks

The message handler for <b>MCIWndSendString</b> (and <b>MCIWNDM_SENDSTRING</b>) appends a device alias to the MCI command you send to the device. Therefore, you should not use any alias in an MCI command that you issue with <b>MCIWndSendString</b>.

To get the return string, which contains the result of the command, use the <a href="/windows/desktop/api/vfw/nf-vfw-mciwndreturnstring">MCIWndReturnString</a> macro.

## -see-also

<a href="/windows/desktop/Multimedia/multimedia-command-strings">Multimedia Command Strings</a>

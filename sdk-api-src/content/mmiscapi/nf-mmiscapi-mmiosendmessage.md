---
UID: NF:mmiscapi.mmioSendMessage
title: mmioSendMessage function (mmiscapi.h)
description: The mmioSendMessage function sends a message to the I/O procedure associated with the specified file.
helpviewer_keywords: ["_win32_mmioSendMessage","mmioSendMessage","mmioSendMessage function [Windows Multimedia]","mmsystem/mmioSendMessage","multimedia.mmiosendmessage"]
old-location: multimedia\mmiosendmessage.htm
tech.root: Multimedia
ms.assetid: 6ff058bf-0681-4ab8-abea-ee820359f4b3
ms.date: 12/05/2018
ms.keywords: _win32_mmioSendMessage, mmioSendMessage, mmioSendMessage function [Windows Multimedia], mmsystem/mmioSendMessage, multimedia.mmiosendmessage
req.header: mmiscapi.h
req.include-header: Mmiscapi.h, Windows.h
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
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - mmioSendMessage
 - mmiscapi/mmioSendMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-misc-l1-1-0.dll
 - winmmbase.dll
 - API-MS-Win-mm-misc-l1-1-1.dll
api_name:
 - mmioSendMessage
---

# mmioSendMessage function


## -description

The <b>mmioSendMessage</b> function sends a message to the I/O procedure associated with the specified file.

## -parameters

### -param hmmio

File handle for a file opened by using the <a href="/previous-versions/dd757331(v=vs.85)">mmioOpen</a> function.

### -param uMsg

Message to send to the I/O procedure.

### -param lParam1

Parameter for the message.

### -param lParam2

Parameter for the message.

## -returns

Returns a value that corresponds to the message. If the I/O procedure does not recognize the message, the return value should be zero.

## -remarks

Use this function to send custom user-defined messages. Do not use it to send the MMIOM_OPEN, MMIOM_CLOSE, MMIOM_READ, MMIOM_WRITE, MMIOM_WRITEFLUSH, or MMIOM_SEEK messages. Define custom messages to be greater than or equal to the MMIOM_USER constant.
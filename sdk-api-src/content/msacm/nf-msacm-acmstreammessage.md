---
UID: NF:msacm.acmStreamMessage
title: acmStreamMessage function (msacm.h)
description: The acmStreamMessage function sends a driver-specific message to an ACM driver.
helpviewer_keywords: ["_win32_acmStreamMessage","acmStreamMessage","acmStreamMessage function [Windows Multimedia]","msacm/acmStreamMessage","multimedia.acmstreammessage"]
old-location: multimedia\acmstreammessage.htm
tech.root: Multimedia
ms.assetid: 30f77126-a874-4014-bbde-ce194da2c61c
ms.date: 12/05/2018
ms.keywords: _win32_acmStreamMessage, acmStreamMessage, acmStreamMessage function [Windows Multimedia], msacm/acmStreamMessage, multimedia.acmstreammessage
req.header: msacm.h
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
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - acmStreamMessage
 - msacm/acmStreamMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msacm32.dll
 - Ext-MS-Win-mm-msacm-l1-1-0.dll
api_name:
 - acmStreamMessage
---

# acmStreamMessage function


## -description

The <b>acmStreamMessage</b> function sends a driver-specific message to an ACM driver.

## -parameters

### -param has

Handle to an open conversion stream.

### -param uMsg

Message to send.

### -param lParam1

Message parameter.

### -param lParam2

Message parameter.

## -returns

Returns the value returned by the ACM device driver.

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>
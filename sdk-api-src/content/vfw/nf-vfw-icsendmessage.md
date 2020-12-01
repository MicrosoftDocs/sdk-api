---
UID: NF:vfw.ICSendMessage
title: ICSendMessage function (vfw.h)
description: The ICSendMessage function sends a message to a compressor.
helpviewer_keywords: ["ICSendMessage","ICSendMessage function [Windows Multimedia]","_win32_ICSendMessage","multimedia.icsendmessage","vfw/ICSendMessage"]
old-location: multimedia\icsendmessage.htm
tech.root: Multimedia
ms.assetid: 0f9c37a9-4bf7-4c49-8a6a-81fbfa76d096
ms.date: 12/05/2018
ms.keywords: ICSendMessage, ICSendMessage function [Windows Multimedia], _win32_ICSendMessage, multimedia.icsendmessage, vfw/ICSendMessage
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
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICSendMessage
 - vfw/ICSendMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - ICSendMessage
---

# ICSendMessage function


## -description

The <b>ICSendMessage</b> function sends a message to a compressor.

## -parameters

### -param hic

Handle to the compressor to receive the message.

### -param msg

Message to send.

### -param dw1

Additional message-specific information.

### -param dw2

Additional message-specific information.

## -returns

Returns a message-specific result.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
---
UID: NF:ws2spi.WPUPostMessage
title: WPUPostMessage function (ws2spi.h)
description: The WPUPostMessage function performs the standard Windows PostMessage function in a way that maintains backward compatibility with older versions of WSOCK32.dll.
helpviewer_keywords: ["WPUPostMessage","WPUPostMessage function [Winsock]","_win32_wpupostmessage_2","winsock.wpupostmessage_2","ws2spi/WPUPostMessage"]
old-location: winsock\wpupostmessage_2.htm
tech.root: WinSock
ms.assetid: f4241941-c39f-441e-aad4-b84f2f8ed828
ms.date: 12/05/2018
ms.keywords: WPUPostMessage, WPUPostMessage function [Winsock], _win32_wpupostmessage_2, winsock.wpupostmessage_2, ws2spi/WPUPostMessage
req.header: ws2spi.h
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
 - WPUPostMessage
 - ws2spi/WPUPostMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - WPUPostMessage
---

# WPUPostMessage function


## -description

The 
**WPUPostMessage** function performs the standard Windows <a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a> function in a way that maintains backward compatibility with older versions of WSOCK32.dll.

## -parameters

### -param hWnd [in]

Handle to the window that will receive the message.

### -param Msg [in]

Message that will be posted.

### -param wParam [in]

First parameter containing additional message-specific information.

### -param lParam [in]

Second parameter containing additional message-specific information.

## -returns

If no error occurs, 
**WPUPostMessage** returns the **TRUE** value. Otherwise, the **FALSE** value is returned.


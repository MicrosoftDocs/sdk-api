---
UID: NF:ws2spi.WPUPostMessage
title: WPUPostMessage function
author: windows-sdk-content
description: The WPUPostMessage function performs the standard Windows PostMessage function in a way that maintains backward compatibility with older versions of WSOCK32.dll.
old-location: winsock\wpupostmessage_2.htm
old-project: winsock
ms.assetid: f4241941-c39f-441e-aad4-b84f2f8ed828
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: WPUPostMessage, WPUPostMessage function [Winsock], _win32_wpupostmessage_2, winsock.wpupostmessage_2, ws2spi/WPUPostMessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WSC_PROVIDER_INFO_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ws2spi.h
api_name:
 - WPUPostMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WPUPostMessage function


## -description



			The 
<b>WPUPostMessage</b> function performs the standard Windows <a href="_win32_postmessage_cpp">PostMessage</a> function in a way that maintains backward compatibility with older versions of WSOCK32.dll.


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
<b>WPUPostMessage</b> returns the <b>TRUE</b> value. Otherwise, the <b>FALSE</b> value is returned.




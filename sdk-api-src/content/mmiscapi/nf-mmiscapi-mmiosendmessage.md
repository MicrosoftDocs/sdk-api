---
UID: NF:mmiscapi.mmioSendMessage
title: mmioSendMessage function
author: windows-sdk-content
description: The mmioSendMessage function sends a message to the I/O procedure associated with the specified file.
old-location: multimedia\mmiosendmessage.htm
tech.root: Multimedia
ms.assetid: 6ff058bf-0681-4ab8-abea-ee820359f4b3
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: "_win32_mmioSendMessage, mmioSendMessage, mmioSendMessage function [Windows Multimedia], mmsystem/mmioSendMessage, multimedia.mmiosendmessage"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# mmioSendMessage function


## -description



The <b>mmioSendMessage</b> function sends a message to the I/O procedure associated with the specified file.




## -parameters




### -param hmmio

File handle for a file opened by using the <a href="https://msdn.microsoft.com/7361f0f2-1c3c-49f1-aec1-2927e05ef0f0">mmioOpen</a> function.


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




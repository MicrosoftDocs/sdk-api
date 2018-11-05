---
UID: NF:vfw.ICSendMessage
title: ICSendMessage function
author: windows-sdk-content
description: The ICSendMessage function sends a message to a compressor.
old-location: multimedia\icsendmessage.htm
tech.root: Multimedia
ms.assetid: 0f9c37a9-4bf7-4c49-8a6a-81fbfa76d096
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ICSendMessage, ICSendMessage function [Windows Multimedia], _win32_ICSendMessage, multimedia.icsendmessage, vfw/ICSendMessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - ICSendMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 


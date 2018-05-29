---
UID: NF:tsvirtualchannels.IWTSVirtualChannel.Write
title: IWTSVirtualChannel::Write
author: windows-sdk-content
description: Starts a write request on the channel.
old-location: termserv\iwtsvirtualchannel_write.htm
old-project: TermServ
ms.assetid: fef7067c-6d81-42b7-8534-191bc98906d4
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IWTSVirtualChannel interface [Remote Desktop Services],Write method, IWTSVirtualChannel.Write, IWTSVirtualChannel::Write, Write, Write method [Remote Desktop Services], Write method [Remote Desktop Services],IWTSVirtualChannel interface, termserv.iwtsvirtualchannel_write, tsvirtualchannels/IWTSVirtualChannel::Write
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tsvirtualchannels.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TsVirtualChannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WTSSBX_SESSION_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	TsVirtualChannels.h
api_name:
-	IWTSVirtualChannel.Write
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IWTSVirtualChannel::Write


## -description


Starts a write request on the channel. All writes are considered asynchronous. Calling this method copies the contents of <i>pBuffer</i> and returns immediately, so  the buffer can be reclaimed. Because of the memory copy, too many <b>Write()</b> calls may result in allocating too much memory by the client.

A <a href="https://msdn.microsoft.com/b900789d-c7da-4974-8c46-72ea8ffd6892">Close()</a> call on this channel will cancel any pending writes.


## -parameters




### -param cbSize [in]

The size, in bytes, of the buffer to which to write.


### -param pBuffer [in]

A pointer to a buffer on the channel to which to write the data. You can reuse this buffer as soon as the call returns.


### -param pReserved [in, optional]

Reserved for future use. The value must be <b>NULL</b>.


## -returns



Returns <b>S_OK</b> if successful.




## -see-also




<a href="https://msdn.microsoft.com/8a5b093f-5756-400f-9442-b95d6010ee46">IWTSVirtualChannel</a>
 

 


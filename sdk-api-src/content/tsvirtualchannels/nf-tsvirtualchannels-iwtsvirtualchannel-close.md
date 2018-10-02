---
UID: NF:tsvirtualchannels.IWTSVirtualChannel.Close
title: IWTSVirtualChannel::Close
author: windows-sdk-content
description: Closes the channel.
old-location: termserv\iwtsvirtualchannel_close.htm
tech.root: TermServ
ms.assetid: b900789d-c7da-4974-8c46-72ea8ffd6892
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Close, Close method [Remote Desktop Services], Close method [Remote Desktop Services],IWTSVirtualChannel interface, IWTSVirtualChannel interface [Remote Desktop Services],Close method, IWTSVirtualChannel.Close, IWTSVirtualChannel::Close, termserv.iwtsvirtualchannel_close, tsvirtualchannels/IWTSVirtualChannel::Close
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TsVirtualChannels.h
api_name:
 - IWTSVirtualChannel.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSVirtualChannel::Close


## -description


Closes the channel.

If the channel has not already been closed, the <b>Close()</b> method will call the <a href="https://msdn.microsoft.com/5038f2f9-980b-4383-a718-eb4e07e9cfe9">IWTSVirtualChannelCallback::OnClose()</a> method into the associated virtual channel callback interface. After a channel is closed, any <a href="https://msdn.microsoft.com/fef7067c-6d81-42b7-8534-191bc98906d4">Write()</a> call on it will fail.


## -parameters






## -returns



Returns <b>S_OK</b> if successful.




## -see-also




<a href="https://msdn.microsoft.com/8a5b093f-5756-400f-9442-b95d6010ee46">IWTSVirtualChannel</a>
 

 


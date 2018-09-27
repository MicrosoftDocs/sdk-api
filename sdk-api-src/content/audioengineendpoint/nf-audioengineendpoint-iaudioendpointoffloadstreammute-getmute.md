---
UID: NF:audioengineendpoint.IAudioEndpointOffloadStreamMute.GetMute
title: IAudioEndpointOffloadStreamMute::GetMute
author: windows-sdk-content
description: The GetMute method retrieves the mute status of the offloaded audio stream.
old-location: coreaudio\iaudioendpointoffloadstreammute_getmute.htm
tech.root: CoreAudio
ms.assetid: 0A8F254B-1287-4633-A14D-7F620CB64818
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetMute, GetMute method [Core Audio], GetMute method [Core Audio],IAudioEndpointOffloadStreamMute interface, IAudioEndpointOffloadStreamMute interface [Core Audio],GetMute method, IAudioEndpointOffloadStreamMute.GetMute, IAudioEndpointOffloadStreamMute::GetMute, audioengineendpoint/IAudioEndpointOffloadStreamMute::GetMute, coreaudio.iaudioendpointoffloadstreammute_getmute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioEndpointOffloadStreamMute.GetMute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioEndpointOffloadStreamMute::GetMute


## -description


The <b>GetMute</b> method retrieves the mute status of the offloaded audio stream.


## -parameters




### -param pbMuted [out]

Indicates whether or not the offloaded audio stream is muted. A value of<b>TRUE</b> indicates that the stream is muted, and a value of<b>FALSE</b> indicates that the stream is not muted.


## -returns



The <b>GetMute</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.




## -see-also




<a href="https://msdn.microsoft.com/F102CBB2-6751-416C-B59B-F91440583594">IAudioEndpointOffloadStreamMute</a>
 

 


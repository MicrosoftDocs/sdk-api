---
UID: NF:dmusics.IDirectMusicSynth.GetChannelPriority
title: IDirectMusicSynth::GetChannelPriority
author: windows-sdk-content
description: The GetChannelPriority method outputs the priority of a MIDI channel.
old-location: audio\idirectmusicsynth_getchannelpriority.htm
tech.root: audio
ms.assetid: be49f7eb-f0ab-48b3-9776-79811309fcee
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetChannelPriority, GetChannelPriority method [Audio Devices], GetChannelPriority method [Audio Devices],IDirectMusicSynth interface, IDirectMusicSynth interface [Audio Devices],GetChannelPriority method, IDirectMusicSynth.GetChannelPriority, IDirectMusicSynth::GetChannelPriority, audio.idirectmusicsynth_getchannelpriority, audmp-routines_9590c152-c9c3-4d0a-aad2-a0884716f681.xml, dmusics/IDirectMusicSynth::GetChannelPriority
ms.topic: method
req.header: dmusics.h
req.include-header: Dmusics.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - dmusics.h
api_name:
 - IDirectMusicSynth.GetChannelPriority
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectMusicSynth::GetChannelPriority


## -description


The <code>GetChannelPriority</code> method outputs the priority of a MIDI channel.


## -parameters




### -param dwChannelGroup

Specifies the channel group that the channel belongs to. This parameter must be one or greater.


### -param dwChannel

Specifies the index of the channel in the channel group. This is a value in the range 0 to 15.


### -param pdwPriority

Output pointer for the priority ranking. This parameter points to a caller-allocated variable into which the method writes the priority ranking value. For a list of the priority values that are defined for this parameter, see the <b>IDirectMusicPort::GetChannelPriority</b> reference page in the Microsoft Windows SDK documentation.


## -returns



<code>GetChannelPriority</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code.




## -remarks



This method is used with the <a href="https://msdn.microsoft.com/6398f460-4c2e-4995-a606-e95e0488f1cd">IDirectMusicSynth::SetChannelPriority</a> method to control the channel priorities and facilitate correct voice stealing.

For more information, see the descriptions of the <b>IDirectMusicPort::GetChannelPriority</b> and <b>IDirectMusicPort::SetChannelPriority</b> methods in the Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/6398f460-4c2e-4995-a606-e95e0488f1cd">IDirectMusicSynth::SetChannelPriority</a>
 

 


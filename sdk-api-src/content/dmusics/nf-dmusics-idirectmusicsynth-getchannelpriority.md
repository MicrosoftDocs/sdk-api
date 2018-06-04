---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



This method is used with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff536542">IDirectMusicSynth::SetChannelPriority</a> method to control the channel priorities and facilitate correct voice stealing.

For more information, see the descriptions of the <b>IDirectMusicPort::GetChannelPriority</b> and <b>IDirectMusicPort::SetChannelPriority</b> methods in the Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536542">IDirectMusicSynth::SetChannelPriority</a>
 

 


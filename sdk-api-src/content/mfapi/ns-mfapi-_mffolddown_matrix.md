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

# _MFFOLDDOWN_MATRIX structure


## -description



Contains coefficients used to transform multichannel audio into a smaller number of audio channels. This process is called <i>fold-down</i>.




## -struct-fields




### -field cbSize

Size of the structure, in bytes.


### -field cSrcChannels

Number of source channels.


### -field cDstChannels

Number of destination channels.


### -field dwChannelMask

Specifies the assignment of audio channels to speaker positions in the transformed audio. This member is a bitwise <b>OR</b> of flags that define the speaker positions. For a list of valid flags, see <a href="https://msdn.microsoft.com/fa5f6baa-0a21-4162-8870-38e71763aba0">MF_MT_AUDIO_CHANNEL_MASK</a> attribute.


### -field Coeff

Array that contains the fold-down coefficients. The number of coefficients is <b>cSrcChannels</b>×<b>cDstChannels</b>. If the number of coefficients is less than the size of the array, the remaining elements in the array are ignored. For more information about how the coefficients are applied, see <a href="http://go.microsoft.com/fwlink/p/?linkid=22396">Windows Media Audio Professional Codec Features</a>.


## -remarks



To specify this information in the media type, set the <a href="https://msdn.microsoft.com/6dfe2b97-1ebc-4954-b478-85b3bbba89e3">MF_MT_AUDIO_FOLDDOWN_MATRIX</a> attribute.

The ASF media source supports fold-down from six channels (5.1 audio) to two channels (stereo). It gets the information from the g_wszFold6To2Channels3 attribute in the ASF header. This attribute is documented in the Windows Media Format SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 


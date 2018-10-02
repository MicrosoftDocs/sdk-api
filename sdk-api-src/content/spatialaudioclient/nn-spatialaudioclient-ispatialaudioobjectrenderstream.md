---
UID: NN:spatialaudioclient.ISpatialAudioObjectRenderStream
title: ISpatialAudioObjectRenderStream
author: windows-sdk-content
description: Provides methods for controlling a spatial audio object render stream, including starting, stopping, and resetting the stream.
old-location: coreaudio\ispatialaudioobjectrenderstream.htm
tech.root: CoreAudio
ms.assetid: B4D10CC6-62BF-4D20-910F-E39DF812010D
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ISpatialAudioObjectRenderStream, ISpatialAudioObjectRenderStream interface [Core Audio], ISpatialAudioObjectRenderStream interface [Core Audio],described, coreaudio.ispatialaudioobjectrenderstream, spatialaudioclient/ISpatialAudioObjectRenderStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: spatialaudioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - spatialaudioclient.h
api_name:
 - ISpatialAudioObjectRenderStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioObjectRenderStream interface


## -description


Provides methods for controlling a spatial audio object render stream, including starting, stopping, and resetting the stream. Also provides methods for activating new <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a> instances and notifying the system when you are beginning and ending the process of updating activated spatial audio objects and data.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioObjectRenderStream</b> interface inherits from <a href="https://msdn.microsoft.com/2C2BE871-EFD1-40E1-B466-6BBD09C56852">ISpatialAudioObjectRenderStreamBase</a>. <b>ISpatialAudioObjectRenderStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioObjectRenderStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1B99E7FB-0796-4902-9B00-470FD08F8AFA">ActivateSpatialAudioObject</a>
</td>
<td align="left" width="63%">
Activates an <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a> for audio rendering.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  Many of the methods provided by this interface are implemented in the inherited <a href="https://msdn.microsoft.com/2C2BE871-EFD1-40E1-B466-6BBD09C56852">ISpatialAudioObjectRenderStreamBase</a> interface.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2C2BE871-EFD1-40E1-B466-6BBD09C56852">ISpatialAudioObjectRenderStreamBase</a>
 

 


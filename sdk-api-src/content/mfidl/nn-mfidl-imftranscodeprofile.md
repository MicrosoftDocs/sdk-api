---
UID: NN:mfidl.IMFTranscodeProfile
title: IMFTranscodeProfile
author: windows-sdk-content
description: Implemented by the transcode profile object.
old-location: mf\imftranscodeprofile.htm
tech.root: medfound
ms.assetid: 82e012e0-84d8-4791-8b6f-bda58b498a90
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: IMFTranscodeProfile, IMFTranscodeProfile interface [Media Foundation], IMFTranscodeProfile interface [Media Foundation],described, mf.imftranscodeprofile, mfidl/IMFTranscodeProfile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - mfidl.h
api_name:
 - IMFTranscodeProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTranscodeProfile interface


## -description


Implemented by the transcode profile object.

The transcode profile stores configuration settings that the topology builder uses to generate the transcode topology for the output file. These configuration settings are specified by the caller and include audio and video stream properties, encoder settings, and  container settings that are specified by the caller.

To create the transcode profile object, call <a href="https://msdn.microsoft.com/2a482c6f-6e20-419a-a7eb-085c41cc8186">MFCreateTranscodeProfile</a>. The configured transcode profile is passed to <a href="https://msdn.microsoft.com/ef3f19bf-1db9-459d-9617-d6cca9d6aba7">MFCreateTranscodeTopology</a>, which creates the transcode topology with the appropriate settings. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTranscodeProfile</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFTranscodeProfile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTranscodeProfile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c02dabfe-33ef-4835-a707-d1350b18629f">GetAudioAttributes</a>
</td>
<td align="left" width="63%">
Gets the audio stream settings that are currently set in the transcode profile.
  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29bf5834-78af-4521-95b1-dfd5764e96fc">GetContainerAttributes</a>
</td>
<td align="left" width="63%">
Gets the container settings that are currently set in the transcode profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/734cb4d0-7017-4a30-9d0c-a6b5ce42fec6">GetVideoAttributes</a>
</td>
<td align="left" width="63%">
Gets the video stream settings that are currently set in the transcode profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4118bb2b-8373-434a-896b-de5a1ba8c793">SetAudioAttributes</a>
</td>
<td align="left" width="63%">
Sets audio stream configuration settings  in the transcode profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c62021cf-85f1-4a85-9263-b7883464f5f8">SetContainerAttributes</a>
</td>
<td align="left" width="63%">
Sets container configuration settings  in the transcode profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e68653c5-5663-4839-a482-2244e147f4b9">SetVideoAttributes</a>
</td>
<td align="left" width="63%">
Sets video stream configuration settings  in the transcode profile. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/52b27359-b319-41a0-88e8-d23567420e92">Fast Transcode Objects</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/24bf68a8-39bf-4302-b28c-71bb23b63469">Transcode API</a>
 

 


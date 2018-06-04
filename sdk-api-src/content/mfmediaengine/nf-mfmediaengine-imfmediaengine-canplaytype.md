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

# IMFMediaEngine::CanPlayType


## -description


Queries how likely it is that the Media Engine can play a specified type of media resource.


## -parameters




### -param type [in]

A string that contains a MIME type with an optional codecs parameter, as defined in RFC 4281.


### -param pAnswer [out]

Receives an <a href="https://msdn.microsoft.com/AABABB09-D45F-474C-B692-DC3592ED164F">MF_MEDIA_ENGINE_CANPLAY</a> enumeration value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method corresponds to the <b>canPlayType</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

The <b>canPlayType</b> attribute defines the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>"" (empty string)</td>
<td>The user-agent cannot play the resource, or the resource type is "application/octet-stream".</td>
</tr>
<tr>
<td>"probably"</td>
<td>The user-agent probably can play the resource.</td>
</tr>
<tr>
<td>"maybe"</td>
<td>Neither of the previous values applies.</td>
</tr>
</table>
 

The value "probably" is used because a MIME type for a media resource is generally not a complete description of the resource. For example, "video/mp4" specifies an MP4 file with video, but does not describe the codec. Even with the optional codecs parameter, the MIME type omits some information, such as the actual coded bit rate. Therefore, it is usually impossible to be certain that playback is possible until the actual media resource is opened.




## -see-also




<a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a>
 

 


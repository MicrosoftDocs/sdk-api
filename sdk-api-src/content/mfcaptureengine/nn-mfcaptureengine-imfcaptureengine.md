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

# IMFCaptureEngine interface


## -description


Controls one or more capture devices. The capture engine implements this interface. To get a pointer to this interface, call either <a href="https://msdn.microsoft.com/4B0C9DD6-135D-4412-A585-7E98A84101B5">MFCreateCaptureEngine</a> or <a href="https://msdn.microsoft.com/D5E7D96B-9438-4332-AD05-249D2DA2481A">IMFCaptureEngineClassFactory::CreateInstance</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCaptureEngine</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFCaptureEngine</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFCaptureEngine</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7DAF5EA3-BA65-4CF9-B7BA-B427A48BF3BC">GetSink</a>
</td>
<td align="left" width="63%">
Gets a pointer to one of the capture sink objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9DED11CA-BDBB-4E1A-BAD1-2EB6216543F9">GetSource</a>
</td>
<td align="left" width="63%">
Gets a pointer to the capture source object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the capture engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C5BCF990-E7F9-48E9-B082-79953F5ED27C">StartPreview</a>
</td>
<td align="left" width="63%">
Starts preview.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff542695">StartRecord</a>
</td>
<td align="left" width="63%">
Starts recording audio and/or video to a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36DE5079-D4D5-4FC5-8CF6-1F5B3F9E8B66">StopPreview</a>
</td>
<td align="left" width="63%">
Stops preview.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff542707">StopRecord</a>
</td>
<td align="left" width="63%">
Stops recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6E633E90-9C8B-44B6-9149-704872143147">TakePhoto</a>
</td>
<td align="left" width="63%">
Captures a still image from the video stream.

</td>
</tr>
</table> 


## -remarks



<b>IMFCaptureEngine</b> only supports one pass CBR encoding.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 


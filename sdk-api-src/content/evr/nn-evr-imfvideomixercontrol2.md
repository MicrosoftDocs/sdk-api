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

# IMFVideoMixerControl2 interface


## -description


Controls preferences for video deinterlacing.



The default video mixer for the <a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a> (EVR) implements this interface.

To get a pointer to the interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> on any of the following objects, using the <b>MR_VIDEO_MIXER_SERVICE</b> service identifier:
<ul>
<li>The <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a>, if the topology contains an instance of the EVR.</li>
<li>The EVR media sink.</li>
<li>The  DirectShow EVR filter.</li>
<li>The EVR mixer.</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoMixerControl2</b> interface inherits from <a href="https://msdn.microsoft.com/8b5f54e3-c6da-4201-857a-9c718ad911db">IMFVideoMixerControl</a>. <b>IMFVideoMixerControl2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoMixerControl2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ec03db2-9e7f-4a11-8d69-7654391a33d8">GetMixingPrefs</a>
</td>
<td align="left" width="63%">
Gets the current preferences for video deinterlacing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae8fa85a-bdae-4fbf-b9d4-a987eb1c4c41">SetMixingPrefs</a>
</td>
<td align="left" width="63%">
Sets the preferences for video deinterlacing.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8b5f54e3-c6da-4201-857a-9c718ad911db">IMFVideoMixerControl</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/3617adf2-ed7b-4788-abce-58bc22a14511">Video Quality Management</a>
 

 


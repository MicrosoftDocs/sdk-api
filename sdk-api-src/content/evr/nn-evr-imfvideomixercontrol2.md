---
UID: NN:evr.IMFVideoMixerControl2
title: IMFVideoMixerControl2
author: windows-sdk-content
description: Controls preferences for video deinterlacing.
old-location: mf\imfvideomixercontrol2.htm
old-project: medfound
ms.assetid: a238b050-101d-4b8a-9479-984b889823f4
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IMFVideoMixerControl2, IMFVideoMixerControl2 interface [Media Foundation], IMFVideoMixerControl2 interface [Media Foundation],described, evr/IMFVideoMixerControl2, mf.imfvideomixercontrol2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: evr.h
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
tech.root: 
req.typenames: MFVideoMixPrefs
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - evr.h
api_name:
 - IMFVideoMixerControl2
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 


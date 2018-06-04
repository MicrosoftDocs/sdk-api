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

# IAMTVAudio interface


## -description



The <code>IAMTVAudio</code> interface controls audio from a television source. The <a href="https://msdn.microsoft.com/882e03d4-5574-4b0f-b965-63ff9dbb7852">TV Audio</a> filter implements this interface. Applications can use it to control television audio settings, including secondary audio program (SAP) and stereo or mono selection.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMTVAudio</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMTVAudio</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMTVAudio</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa2e71f3-3aa0-4260-925d-579006459a09">get_TVAudioMode</a>
</td>
<td align="left" width="63%">
Retrieves the current TV audio mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c64dc038-7ebf-4aa4-a7ae-b3eb0e8eaf1a">GetAvailableTVAudioModes</a>
</td>
<td align="left" width="63%">
Retrieves a bitmask of the possible modes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c67abc9-2419-473b-a2e6-4fc7df50752c">GetHardwareSupportedTVAudioModes</a>
</td>
<td align="left" width="63%">
Retrieves a bitmask of the formats available in the hardware.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7efe43af-db07-4286-b0b7-6527403568f0">put_TVAudioMode</a>
</td>
<td align="left" width="63%">
Sets the current TV audio mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfd8d0b3-e90f-4f77-9a26-0a4db03041ee">RegisterNotificationCallBack</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17a2f882-f6a8-467d-a6f9-eb8e6309e878">UnRegisterNotificationCallBack</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9f2c18ec-3684-42a8-a3df-5f8827b27642">Analog Television</a>
 

 


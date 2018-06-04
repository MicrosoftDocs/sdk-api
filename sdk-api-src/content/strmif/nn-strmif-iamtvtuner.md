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

# IAMTVTuner interface


## -description



The <code>IAMTVTuner</code> interface controls a TV tuner. The <a href="https://msdn.microsoft.com/a8e101dc-78ab-495f-9086-7b1d1e87c357">TV Tuner</a> filter implements this interface. Applications can use this interface to set TV channels and to get or set information about their frequencies, and to determine what analog video standards your TV tuner card supports.

The interface supports tuners for analog broadcast television and AM/FM radio. It supports tuners with multiple input pins, to enable multiple devices and multiple transmission types. The TV Tuner filter supports worldwide tuning coverage. It maps TV channels to specific frequencies through the <a href="https://msdn.microsoft.com/47ad4288-d855-41cd-b8a2-7b3733a87b41">IAMTuner::put_Channel</a> and <a href="https://msdn.microsoft.com/ae8338e4-b75d-42d5-bcb7-84352921458c">IAMTVTuner::AutoTune</a> methods. These methods handle the details of the conversion, so that the hardware driver receives an exact frequency.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMTVTuner</b> interface inherits from <a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner</a>. <b>IAMTVTuner</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMTVTuner</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae8338e4-b75d-42d5-bcb7-84352921458c">AutoTune</a>
</td>
<td align="left" width="63%">
Scans for a precise signal on the channel's frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d0d288a-7ad0-40ad-b86e-9df9447ed484">get_AudioFrequency</a>
</td>
<td align="left" width="63%">
Retrieves the current audio frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b1a31d4-be05-4ab3-8ca3-b1a3f4bda03f">get_AvailableTVFormats</a>
</td>
<td align="left" width="63%">
Retrieves all the analog video TV standards that the tuner supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9dbcdc9f-7efe-4784-a60c-a6c161befb9b">get_ConnectInput</a>
</td>
<td align="left" width="63%">
Retrieves the hardware tuner input connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49763cc3-be8b-4620-b99f-af787844c97c">get_InputType</a>
</td>
<td align="left" width="63%">
Retrieves the input type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06841331-3b85-4532-8c0c-96022885f92c">get_NumInputConnections</a>
</td>
<td align="left" width="63%">
Retrieves the number of TV sources plugged into the tuner filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26e20511-04f6-4713-967f-5828e6f2a46d">get_TVFormat</a>
</td>
<td align="left" width="63%">
Retrieves the current analog video TV standard in use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d19552ce-1314-4217-9bd3-72369b4334cf">get_VideoFrequency</a>
</td>
<td align="left" width="63%">
Retrieves the current video frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0ea5d82-acb6-401a-942a-99d34058c648">put_ConnectInput</a>
</td>
<td align="left" width="63%">
Sets the hardware tuner input connection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d23df6b1-eddc-4c8c-a3c9-400f915e35c4">put_InputType</a>
</td>
<td align="left" width="63%">
Sets the tuner input type (cable or antenna).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e39d757-d8bd-4011-9a67-6bf57b5d820b">StoreAutoTune</a>
</td>
<td align="left" width="63%">
Saves the fine-tuning information for all channels.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9f2c18ec-3684-42a8-a3df-5f8827b27642">Analog Television</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner</a>
 

 


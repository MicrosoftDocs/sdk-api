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

# IPerChannelDbLevel::GetLevelRange


## -description



The <b>GetLevelRange</b> method gets the range, in decibels, of the volume level of the specified channel.




## -parameters




### -param nChannel [in]

The number of the selected channel. If the audio stream has <i>n</i> channels, the channels are numbered from 0 to <i>n</i>– 1. To get the number of channels in the stream, call the <a href="https://msdn.microsoft.com/f8c6c0fd-fe29-467a-936e-f83c6d951bdd">IPerChannelDbLevel::GetChannelCount</a> method.


### -param pfMinLevelDB [out]

Pointer to a <b>float</b> variable into which the method writes the minimum volume level in decibels.


### -param pfMaxLevelDB [out]

Pointer to a <b>float</b> variable into which the method writes the maximum volume level in decibels.


### -param pfStepping [out]

Pointer to a <b>float</b> variable into which the method writes the stepping value between consecutive volume levels in the range  <i>*pfMinLevelDB</i> to  <i>*pfMaxLevelDB</i>. If the difference between the maximum and minimum volume levels is <i>d</i> decibels, and the range is divided into <i>n</i> steps (uniformly sized intervals), then the volume can have <i>n</i> + 1 discrete levels and the size of the step between consecutive levels is <i>d</i> / <i>n</i> decibels.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>nChannel</i> is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pfminLevelDB</i>, <i>pfmaxLevelDB</i>, or <i>pfmaxLevelDB</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e70b4518-c9de-4426-b8e5-db80656699a9">IPerChannelDbLevel Interface</a>



<a href="https://msdn.microsoft.com/f8c6c0fd-fe29-467a-936e-f83c6d951bdd">IPerChannelDbLevel::GetChannelCount</a>
 

 


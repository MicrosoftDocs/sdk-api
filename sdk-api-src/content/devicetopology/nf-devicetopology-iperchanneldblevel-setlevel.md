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

# IPerChannelDbLevel::SetLevel


## -description



The <b>SetLevel</b> method sets the volume level, in decibels, of the specified channel.




## -parameters




### -param nChannel [in]

The number of the selected channel. If the audio stream has <i>N</i> channels, the channels are numbered from 0 to <i>N</i>– 1. To get the number of channels in the stream, call the <a href="https://msdn.microsoft.com/f8c6c0fd-fe29-467a-936e-f83c6d951bdd">IPerChannelDbLevel::GetChannelCount</a> method.


### -param fLevelDB [in]

The new volume level in decibels. A positive value represents gain, and a negative value represents attenuation.


### -param pguidEventContext [in]

Context value for the <a href="https://msdn.microsoft.com/a2f32cb9-3c8b-4b44-96a2-dd70afcca71a">IControlChangeNotify::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetLevel</b> call changes the state of the level control, all clients that have registered <a href="https://msdn.microsoft.com/e50e13c2-1ef3-46f6-8c53-f99cc1631a79">IControlChangeNotify</a> interfaces with that control receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the control-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 




## -remarks



If the caller specifies a value for <i>fLevelDB</i> that is an exact stepping value, the <b>SetLevel</b> method completes successfully. A subsequent call to the <a href="https://msdn.microsoft.com/afc76c80-1656-4f06-8024-c9b041f52e64">IPerChannelDbLevel::GetLevel</a> method will return either the value that was set, or one of the following values:<ul>
<li>If the set value was below the minimum, the <b>GetLevel</b> method returns the minimum value.</li>
<li>If the set value was above the maximum, the <b>GetLevel</b> method returns the maximum value.</li>
<li>If the set value was between two stepping values, the <b>GetLevel</b> method returns a value that could be the next stepping value above or the stepping value below the set value; the relative distances from the set value to the neighboring stepping values is unimportant. The value that the <b>GetLevel</b> method returns is whichever value has more of an impact on the signal path.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/e70b4518-c9de-4426-b8e5-db80656699a9">IPerChannelDbLevel Interface</a>



<a href="https://msdn.microsoft.com/f8c6c0fd-fe29-467a-936e-f83c6d951bdd">IPerChannelDbLevel::GetChannelCount</a>



<a href="https://msdn.microsoft.com/afc76c80-1656-4f06-8024-c9b041f52e64">IPerChannelDbLevel::GetLevel</a>



<a href="https://msdn.microsoft.com/492eddb0-f8f2-4639-b5fe-1d02bf8c983a">IPerChannelDbLevel::GetLevelRange</a>
 

 


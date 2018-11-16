---
UID: NF:devicetopology.IPerChannelDbLevel.SetLevelAllChannels
title: IPerChannelDbLevel::SetLevelAllChannels
author: windows-sdk-content
description: The SetLevelAllChannels method sets the volume levels, in decibels, of all the channels in the audio stream.
old-location: coreaudio\iperchanneldblevel_setlevelallchannels.htm
tech.root: CoreAudio
ms.assetid: 92c06b38-954d-4bab-b4ea-0f30e64aa9e4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IPerChannelDbLevel interface [Core Audio],SetLevelAllChannels method, IPerChannelDbLevel.SetLevelAllChannels, IPerChannelDbLevel::SetLevelAllChannels, IPerChannelDbLevelSetLevelAllChannels, SetLevelAllChannels, SetLevelAllChannels method [Core Audio], SetLevelAllChannels method [Core Audio],IPerChannelDbLevel interface, coreaudio.iperchanneldblevel_setlevelallchannels, devicetopology/IPerChannelDbLevel::SetLevelAllChannels
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Devicetopology.h
api_name:
 - IPerChannelDbLevel.SetLevelAllChannels
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- devicetopology.h
: 
- IPerChannelDbLevel.SetLevelAllChannels
: 
---

# IPerChannelDbLevel::SetLevelAllChannels


## -description



The <b>SetLevelAllChannels</b> method sets the volume levels, in decibels, of all the channels in the audio stream.




## -parameters




### -param aLevelsDB [in]

Pointer to an array of volume levels. This parameter points to a caller-allocated <b>float</b> array into which the method writes the new volume levels, in decibels, for all the channels. The method writes the level for a particular channel into the array element whose index matches the channel number. If the audio stream contains <i>n</i> channels, the channels are numbered 0 to <i>n</i>– 1. To get the number of channels in the stream, call the <a href="https://msdn.microsoft.com/f8c6c0fd-fe29-467a-936e-f83c6d951bdd">IPerChannelDbLevel::GetChannelCount</a> method.


### -param cChannels [in]

The number of elements in the <i>aLevelsDB</i> array. If this parameter does not match the number of channels in the audio stream, the method fails without modifying the <i>aLevelsDB</i> array.


### -param pguidEventContext [in]

Context value for the <a href="https://msdn.microsoft.com/a2f32cb9-3c8b-4b44-96a2-dd70afcca71a">IControlChangeNotify::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetLevelAllChannels</b> call changes the state of the level control, all clients that have registered <a href="https://msdn.microsoft.com/e50e13c2-1ef3-46f6-8c53-f99cc1631a79">IControlChangeNotify</a> interfaces with that control receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the control-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.


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
Parameter <i>cChannels</i> does not equal the number of channels.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>aLevelsDB</i> is <b>NULL</b>.

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



If the specified level value for any channel is beyond the range that the <a href="https://msdn.microsoft.com/492eddb0-f8f2-4639-b5fe-1d02bf8c983a">IPerChannelDbLevel::GetLevelRange</a> method reports for that channel, the <b>SetLevelAllChannels</b> call clamps the value to the supported range and completes successfully. A subsequent call to the <a href="https://msdn.microsoft.com/afc76c80-1656-4f06-8024-c9b041f52e64">IPerChannelDbLevel::GetLevel</a> method retrieves the actual value used for that channel.




## -see-also




<a href="https://msdn.microsoft.com/e70b4518-c9de-4426-b8e5-db80656699a9">IPerChannelDbLevel Interface</a>



<a href="https://msdn.microsoft.com/f8c6c0fd-fe29-467a-936e-f83c6d951bdd">IPerChannelDbLevel::GetChannelCount</a>



<a href="https://msdn.microsoft.com/afc76c80-1656-4f06-8024-c9b041f52e64">IPerChannelDbLevel::GetLevel</a>



<a href="https://msdn.microsoft.com/492eddb0-f8f2-4639-b5fe-1d02bf8c983a">IPerChannelDbLevel::GetLevelRange</a>
 

 


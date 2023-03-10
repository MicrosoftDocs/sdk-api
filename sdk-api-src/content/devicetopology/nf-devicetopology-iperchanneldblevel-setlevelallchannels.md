---
UID: NF:devicetopology.IPerChannelDbLevel.SetLevelAllChannels
title: IPerChannelDbLevel::SetLevelAllChannels (devicetopology.h)
description: The SetLevelAllChannels method sets the volume levels, in decibels, of all the channels in the audio stream.
helpviewer_keywords: ["IPerChannelDbLevel interface [Core Audio]","SetLevelAllChannels method","IPerChannelDbLevel.SetLevelAllChannels","IPerChannelDbLevel::SetLevelAllChannels","IPerChannelDbLevelSetLevelAllChannels","SetLevelAllChannels","SetLevelAllChannels method [Core Audio]","SetLevelAllChannels method [Core Audio]","IPerChannelDbLevel interface","coreaudio.iperchanneldblevel_setlevelallchannels","devicetopology/IPerChannelDbLevel::SetLevelAllChannels"]
old-location: coreaudio\iperchanneldblevel_setlevelallchannels.htm
tech.root: CoreAudio
ms.assetid: 92c06b38-954d-4bab-b4ea-0f30e64aa9e4
ms.date: 12/05/2018
ms.keywords: IPerChannelDbLevel interface [Core Audio],SetLevelAllChannels method, IPerChannelDbLevel.SetLevelAllChannels, IPerChannelDbLevel::SetLevelAllChannels, IPerChannelDbLevelSetLevelAllChannels, SetLevelAllChannels, SetLevelAllChannels method [Core Audio], SetLevelAllChannels method [Core Audio],IPerChannelDbLevel interface, coreaudio.iperchanneldblevel_setlevelallchannels, devicetopology/IPerChannelDbLevel::SetLevelAllChannels
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPerChannelDbLevel::SetLevelAllChannels
 - devicetopology/IPerChannelDbLevel::SetLevelAllChannels
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IPerChannelDbLevel.SetLevelAllChannels
---

# IPerChannelDbLevel::SetLevelAllChannels


## -description

The <b>SetLevelAllChannels</b> method sets the volume levels, in decibels, of all the channels in the audio stream.

## -parameters

### -param aLevelsDB [in]

Pointer to an array of volume levels. This parameter points to a caller-allocated <b>float</b> array into which the method writes the new volume levels, in decibels, for all the channels. The method writes the level for a particular channel into the array element whose index matches the channel number. If the audio stream contains <i>n</i> channels, the channels are numbered 0 to <i>n</i>– 1. To get the number of channels in the stream, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getchannelcount">IPerChannelDbLevel::GetChannelCount</a> method.

### -param cChannels [in]

The number of elements in the <i>aLevelsDB</i> array. If this parameter does not match the number of channels in the audio stream, the method fails without modifying the <i>aLevelsDB</i> array.

### -param pguidEventContext [in]

Context value for the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-icontrolchangenotify-onnotify">IControlChangeNotify::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetLevelAllChannels</b> call changes the state of the level control, all clients that have registered <a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolchangenotify">IControlChangeNotify</a> interfaces with that control receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the control-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.

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

If the specified level value for any channel is beyond the range that the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getlevelrange">IPerChannelDbLevel::GetLevelRange</a> method reports for that channel, the <b>SetLevelAllChannels</b> call clamps the value to the supported range and completes successfully. A subsequent call to the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getlevel">IPerChannelDbLevel::GetLevel</a> method retrieves the actual value used for that channel.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iperchanneldblevel">IPerChannelDbLevel Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getchannelcount">IPerChannelDbLevel::GetChannelCount</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getlevel">IPerChannelDbLevel::GetLevel</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getlevelrange">IPerChannelDbLevel::GetLevelRange</a>
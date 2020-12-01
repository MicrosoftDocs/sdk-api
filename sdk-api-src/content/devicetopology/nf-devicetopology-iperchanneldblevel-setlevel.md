---
UID: NF:devicetopology.IPerChannelDbLevel.SetLevel
title: IPerChannelDbLevel::SetLevel (devicetopology.h)
description: The SetLevel method sets the volume level, in decibels, of the specified channel.
helpviewer_keywords: ["IPerChannelDbLevel interface [Core Audio]","SetLevel method","IPerChannelDbLevel.SetLevel","IPerChannelDbLevel::SetLevel","IPerChannelDbLevelSetLevel","SetLevel","SetLevel method [Core Audio]","SetLevel method [Core Audio]","IPerChannelDbLevel interface","coreaudio.iperchanneldblevel_setlevel","devicetopology/IPerChannelDbLevel::SetLevel"]
old-location: coreaudio\iperchanneldblevel_setlevel.htm
tech.root: CoreAudio
ms.assetid: 103efe46-bca5-40a7-815b-d2a1f6e29cbc
ms.date: 12/05/2018
ms.keywords: IPerChannelDbLevel interface [Core Audio],SetLevel method, IPerChannelDbLevel.SetLevel, IPerChannelDbLevel::SetLevel, IPerChannelDbLevelSetLevel, SetLevel, SetLevel method [Core Audio], SetLevel method [Core Audio],IPerChannelDbLevel interface, coreaudio.iperchanneldblevel_setlevel, devicetopology/IPerChannelDbLevel::SetLevel
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
 - IPerChannelDbLevel::SetLevel
 - devicetopology/IPerChannelDbLevel::SetLevel
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
 - IPerChannelDbLevel.SetLevel
---

# IPerChannelDbLevel::SetLevel


## -description

The <b>SetLevel</b> method sets the volume level, in decibels, of the specified channel.

## -parameters

### -param nChannel [in]

The number of the selected channel. If the audio stream has <i>N</i> channels, the channels are numbered from 0 to <i>N</i>– 1. To get the number of channels in the stream, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getchannelcount">IPerChannelDbLevel::GetChannelCount</a> method.

### -param fLevelDB [in]

The new volume level in decibels. A positive value represents gain, and a negative value represents attenuation.

### -param pguidEventContext [in]

Context value for the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-icontrolchangenotify-onnotify">IControlChangeNotify::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetLevel</b> call changes the state of the level control, all clients that have registered <a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolchangenotify">IControlChangeNotify</a> interfaces with that control receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the control-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.

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

If the caller specifies a value for <i>fLevelDB</i> that is an exact stepping value, the <b>SetLevel</b> method completes successfully. A subsequent call to the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getlevel">IPerChannelDbLevel::GetLevel</a> method will return either the value that was set, or one of the following values:<ul>
<li>If the set value was below the minimum, the <b>GetLevel</b> method returns the minimum value.</li>
<li>If the set value was above the maximum, the <b>GetLevel</b> method returns the maximum value.</li>
<li>If the set value was between two stepping values, the <b>GetLevel</b> method returns a value that could be the next stepping value above or the stepping value below the set value; the relative distances from the set value to the neighboring stepping values is unimportant. The value that the <b>GetLevel</b> method returns is whichever value has more of an impact on the signal path.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iperchanneldblevel">IPerChannelDbLevel Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getchannelcount">IPerChannelDbLevel::GetChannelCount</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getlevel">IPerChannelDbLevel::GetLevel</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getlevelrange">IPerChannelDbLevel::GetLevelRange</a>
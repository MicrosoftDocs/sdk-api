---
UID: NF:devicetopology.IPerChannelDbLevel.SetLevelUniform
title: IPerChannelDbLevel::SetLevelUniform (devicetopology.h)
description: The SetLevelUniform method sets all channels in the audio stream to the same uniform volume level, in decibels.
helpviewer_keywords: ["IPerChannelDbLevel interface [Core Audio]","SetLevelUniform method","IPerChannelDbLevel.SetLevelUniform","IPerChannelDbLevel::SetLevelUniform","IPerChannelDbLevelSetLevelUniform","SetLevelUniform","SetLevelUniform method [Core Audio]","SetLevelUniform method [Core Audio]","IPerChannelDbLevel interface","coreaudio.iperchanneldblevel_setleveluniform","devicetopology/IPerChannelDbLevel::SetLevelUniform"]
old-location: coreaudio\iperchanneldblevel_setleveluniform.htm
tech.root: CoreAudio
ms.assetid: b78bebcb-d32b-4eda-a805-35d4459b6b4f
ms.date: 12/05/2018
ms.keywords: IPerChannelDbLevel interface [Core Audio],SetLevelUniform method, IPerChannelDbLevel.SetLevelUniform, IPerChannelDbLevel::SetLevelUniform, IPerChannelDbLevelSetLevelUniform, SetLevelUniform, SetLevelUniform method [Core Audio], SetLevelUniform method [Core Audio],IPerChannelDbLevel interface, coreaudio.iperchanneldblevel_setleveluniform, devicetopology/IPerChannelDbLevel::SetLevelUniform
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
 - IPerChannelDbLevel::SetLevelUniform
 - devicetopology/IPerChannelDbLevel::SetLevelUniform
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
 - IPerChannelDbLevel.SetLevelUniform
---

# IPerChannelDbLevel::SetLevelUniform


## -description

The <b>SetLevelUniform</b> method sets all channels in the audio stream to the same uniform volume level, in decibels.

## -parameters

### -param fLevelDB [in]

The new uniform level in decibels.

### -param pguidEventContext [in]

Context value for the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-icontrolchangenotify-onnotify">IControlChangeNotify::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetLevelUniform</b> call changes the state of the level control, all clients that have registered <a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolchangenotify">IControlChangeNotify</a> interfaces with that control receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the control-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>

## -remarks

If the specified uniform level is beyond the range that the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getlevelrange">IPerChannelDbLevel::GetLevelRange</a> method reports for a particular channel, the <b>SetLevelUniform</b> call clamps the value for that channel to the supported range and completes successfully. A subsequent call to the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getlevel">IPerChannelDbLevel::GetLevel</a> method retrieves the actual value used for that channel.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iperchanneldblevel">IPerChannelDbLevel Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getlevel">IPerChannelDbLevel::GetLevel</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getlevelrange">IPerChannelDbLevel::GetLevelRange</a>
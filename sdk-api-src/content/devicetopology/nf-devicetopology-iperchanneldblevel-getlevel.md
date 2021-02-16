---
UID: NF:devicetopology.IPerChannelDbLevel.GetLevel
title: IPerChannelDbLevel::GetLevel (devicetopology.h)
description: The GetLevel method gets the volume level, in decibels, of the specified channel.
helpviewer_keywords: ["GetLevel","GetLevel method [Core Audio]","GetLevel method [Core Audio]","IPerChannelDbLevel interface","IPerChannelDbLevel interface [Core Audio]","GetLevel method","IPerChannelDbLevel.GetLevel","IPerChannelDbLevel::GetLevel","IPerChannelDbLevelGetLevel","coreaudio.iperchanneldblevel_getlevel","devicetopology/IPerChannelDbLevel::GetLevel"]
old-location: coreaudio\iperchanneldblevel_getlevel.htm
tech.root: CoreAudio
ms.assetid: afc76c80-1656-4f06-8024-c9b041f52e64
ms.date: 12/05/2018
ms.keywords: GetLevel, GetLevel method [Core Audio], GetLevel method [Core Audio],IPerChannelDbLevel interface, IPerChannelDbLevel interface [Core Audio],GetLevel method, IPerChannelDbLevel.GetLevel, IPerChannelDbLevel::GetLevel, IPerChannelDbLevelGetLevel, coreaudio.iperchanneldblevel_getlevel, devicetopology/IPerChannelDbLevel::GetLevel
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
 - IPerChannelDbLevel::GetLevel
 - devicetopology/IPerChannelDbLevel::GetLevel
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
 - IPerChannelDbLevel.GetLevel
---

# IPerChannelDbLevel::GetLevel


## -description

The <b>GetLevel</b> method gets the volume level, in decibels, of the specified channel.

## -parameters

### -param nChannel [in]

The channel number. If the audio stream has <i>N</i> channels, the channels are numbered from 0 to <i>N</i>– 1. To get the number of channels in the stream, call the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getchannelcount">IPerChannelDbLevel::GetChannelCount</a> method.

### -param pfLevelDB [out]

Pointer to a <b>float</b> variable into which the method writes the volume level, in decibels, of the specified channel.

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
Pointer <i>pfLevelDB</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iperchanneldblevel">IPerChannelDbLevel Interface</a>



<a href="/windows/desktop/api/devicetopology/nf-devicetopology-iperchanneldblevel-getchannelcount">IPerChannelDbLevel::GetChannelCount</a>
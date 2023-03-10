---
UID: NF:devicetopology.IPerChannelDbLevel.GetChannelCount
title: IPerChannelDbLevel::GetChannelCount (devicetopology.h)
description: The GetChannelCount method gets the number of channels in the audio stream. (IPerChannelDbLevel.GetChannelCount)
helpviewer_keywords: ["GetChannelCount","GetChannelCount method [Core Audio]","GetChannelCount method [Core Audio]","IPerChannelDbLevel interface","IPerChannelDbLevel interface [Core Audio]","GetChannelCount method","IPerChannelDbLevel.GetChannelCount","IPerChannelDbLevel::GetChannelCount","IPerChannelDbLevelGetChannelCount","coreaudio.iperchanneldblevel_getchannelcount","devicetopology/IPerChannelDbLevel::GetChannelCount"]
old-location: coreaudio\iperchanneldblevel_getchannelcount.htm
tech.root: CoreAudio
ms.assetid: f8c6c0fd-fe29-467a-936e-f83c6d951bdd
ms.date: 12/05/2018
ms.keywords: GetChannelCount, GetChannelCount method [Core Audio], GetChannelCount method [Core Audio],IPerChannelDbLevel interface, IPerChannelDbLevel interface [Core Audio],GetChannelCount method, IPerChannelDbLevel.GetChannelCount, IPerChannelDbLevel::GetChannelCount, IPerChannelDbLevelGetChannelCount, coreaudio.iperchanneldblevel_getchannelcount, devicetopology/IPerChannelDbLevel::GetChannelCount
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
 - IPerChannelDbLevel::GetChannelCount
 - devicetopology/IPerChannelDbLevel::GetChannelCount
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
 - IPerChannelDbLevel.GetChannelCount
---

# IPerChannelDbLevel::GetChannelCount


## -description

The <b>GetChannelCount</b> method gets the number of channels in the audio stream.

## -parameters

### -param pcChannels [out]

Pointer to a <b>UINT</b> variable into which the method writes the channel count (the number of channels in the audio stream).

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pcChannels</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iperchanneldblevel">IPerChannelDbLevel Interface</a>

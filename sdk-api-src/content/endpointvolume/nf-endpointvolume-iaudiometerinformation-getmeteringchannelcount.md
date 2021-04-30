---
UID: NF:endpointvolume.IAudioMeterInformation.GetMeteringChannelCount
title: IAudioMeterInformation::GetMeteringChannelCount (endpointvolume.h)
description: The GetMeteringChannelCount method gets the number of channels in the audio stream that are monitored by peak meters.
helpviewer_keywords: ["GetMeteringChannelCount","GetMeteringChannelCount method [Core Audio]","GetMeteringChannelCount method [Core Audio]","IAudioMeterInformation interface","IAudioMeterInformation interface [Core Audio]","GetMeteringChannelCount method","IAudioMeterInformation.GetMeteringChannelCount","IAudioMeterInformation::GetMeteringChannelCount","IAudioMeterInformationGetMeteringChannelCount","coreaudio.iaudiometerinformation_getmeteringchannelcount","endpointvolume/IAudioMeterInformation::GetMeteringChannelCount"]
old-location: coreaudio\iaudiometerinformation_getmeteringchannelcount.htm
tech.root: CoreAudio
ms.assetid: 6f1deef6-cc47-4736-b0bb-99afb1966895
ms.date: 12/05/2018
ms.keywords: GetMeteringChannelCount, GetMeteringChannelCount method [Core Audio], GetMeteringChannelCount method [Core Audio],IAudioMeterInformation interface, IAudioMeterInformation interface [Core Audio],GetMeteringChannelCount method, IAudioMeterInformation.GetMeteringChannelCount, IAudioMeterInformation::GetMeteringChannelCount, IAudioMeterInformationGetMeteringChannelCount, coreaudio.iaudiometerinformation_getmeteringchannelcount, endpointvolume/IAudioMeterInformation::GetMeteringChannelCount
req.header: endpointvolume.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IAudioMeterInformation::GetMeteringChannelCount
 - endpointvolume/IAudioMeterInformation::GetMeteringChannelCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Endpointvolume.h
api_name:
 - IAudioMeterInformation.GetMeteringChannelCount
---

# IAudioMeterInformation::GetMeteringChannelCount


## -description

The <b>GetMeteringChannelCount</b> method gets the number of channels in the audio stream that are monitored by peak meters.

## -parameters

### -param pnChannelCount [out]

Pointer to a <b>UINT</b> variable into which the method writes the number of channels.

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
Parameter <i>pnChannelCount</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudiometerinformation">IAudioMeterInformation Interface</a>
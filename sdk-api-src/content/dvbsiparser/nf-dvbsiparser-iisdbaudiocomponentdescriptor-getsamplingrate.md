---
UID: NF:dvbsiparser.IIsdbAudioComponentDescriptor.GetSamplingRate
title: IIsdbAudioComponentDescriptor::GetSamplingRate (dvbsiparser.h)
description: Gets the value of the sampling_rate field from a an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. This three-bit field contains a code that indicates the sampling frequency.
helpviewer_keywords: ["GetSamplingRate","GetSamplingRate method [Microsoft TV Technologies]","GetSamplingRate method [Microsoft TV Technologies]","IIsdbAudioComponentDescriptor interface","IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies]","GetSamplingRate method","IIsdbAudioComponentDescriptor.GetSamplingRate","IIsdbAudioComponentDescriptor::GetSamplingRate","dvbsiparser/IIsdbAudioComponentDescriptor::GetSamplingRate","mstv.iisdbaudiocomponentdescriptor_getsamplingrate"]
old-location: mstv\iisdbaudiocomponentdescriptor_getsamplingrate.htm
tech.root: mstv
ms.assetid: ccb31b56-10a1-47ee-9d1b-116d860bef11
ms.date: 12/05/2018
ms.keywords: GetSamplingRate, GetSamplingRate method [Microsoft TV Technologies], GetSamplingRate method [Microsoft TV Technologies],IIsdbAudioComponentDescriptor interface, IIsdbAudioComponentDescriptor interface [Microsoft TV Technologies],GetSamplingRate method, IIsdbAudioComponentDescriptor.GetSamplingRate, IIsdbAudioComponentDescriptor::GetSamplingRate, dvbsiparser/IIsdbAudioComponentDescriptor::GetSamplingRate, mstv.iisdbaudiocomponentdescriptor_getsamplingrate
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IIsdbAudioComponentDescriptor::GetSamplingRate
 - dvbsiparser/IIsdbAudioComponentDescriptor::GetSamplingRate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbAudioComponentDescriptor.GetSamplingRate
---

# IIsdbAudioComponentDescriptor::GetSamplingRate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the value of the sampling_rate field from a an Integrated Services Digital Broadcasting (ISDB) audio component descriptor. This three-bit field contains a code that indicates the sampling frequency.

## -parameters

### -param pbVal [out]

Receives one of the following codes:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>000</dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>001</dt>
</dl>
</td>
<td width="60%">
16 kHz.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>010</dt>
</dl>
</td>
<td width="60%">
22.05 kHz.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>011</dt>
</dl>
</td>
<td width="60%">
24 kHz.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>101</dt>
</dl>
</td>
<td width="60%">
32 kHz.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>110</dt>
</dl>
</td>
<td width="60%">
44.1 kHz.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>111</dt>
</dl>
</td>
<td width="60%">
48 kHz.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbaudiocomponentdescriptor">IIsdbAudioComponentDescriptor</a>
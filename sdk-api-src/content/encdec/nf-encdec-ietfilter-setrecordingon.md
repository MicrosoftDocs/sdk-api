---
UID: NF:encdec.IETFilter.SetRecordingOn
title: IETFilter::SetRecordingOn (encdec.h)
description: The SetRecordingOn method signals to the Encrypter/Tagger filter that the Video Control is about to start or stop recording.
helpviewer_keywords: ["IETFilter interface [Microsoft TV Technologies]","SetRecordingOn method","IETFilter.SetRecordingOn","IETFilter::SetRecordingOn","IETFilterSetRecordingOn","SetRecordingOn","SetRecordingOn method [Microsoft TV Technologies]","SetRecordingOn method [Microsoft TV Technologies]","IETFilter interface","encdec/IETFilter::SetRecordingOn","mstv.ietfilter_setrecordingon"]
old-location: mstv\ietfilter_setrecordingon.htm
tech.root: mstv
ms.assetid: 4579b897-8b68-4b95-8dd4-e5fd94195742
ms.date: 12/05/2018
ms.keywords: IETFilter interface [Microsoft TV Technologies],SetRecordingOn method, IETFilter.SetRecordingOn, IETFilter::SetRecordingOn, IETFilterSetRecordingOn, SetRecordingOn, SetRecordingOn method [Microsoft TV Technologies], SetRecordingOn method [Microsoft TV Technologies],IETFilter interface, encdec/IETFilter::SetRecordingOn, mstv.ietfilter_setrecordingon
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IETFilter::SetRecordingOn
 - encdec/IETFilter::SetRecordingOn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EncDec.h
api_name:
 - IETFilter.SetRecordingOn
---

# IETFilter::SetRecordingOn


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>SetRecordingOn</b> method signals to the Encrypter/Tagger filter that the Video Control is about to start or stop recording.

## -parameters

### -param fRecState

<b>TRUE</b> if recording is about to start, or <b>FALSE</b> if recording is about to stop.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

The <b>SetRecordingOn</b> method enables the Video Control to enforce copy protection in the television broadcast signal. When the Video Control uses the Stream Buffer Engine to play television content, the Encrypter/Tagger filter is located in the Stream Buffer Sink graph. The Encrypter/Tagger sends data to the Stream Buffer Sink for both playback and recording. When <b>SetRecordingOn</b> is called with the value <b>TRUE</b>, the Encrypter/Tagger watches the video stream for the copy protection flags and sends a broadcast event if they change. The Video Control listens for the event and disallows the recording if indicated by the copy protection flag.

## -see-also

<a href="/previous-versions/windows/desktop/api/encdec/nn-encdec-ietfilter">IETFilter Interface</a>
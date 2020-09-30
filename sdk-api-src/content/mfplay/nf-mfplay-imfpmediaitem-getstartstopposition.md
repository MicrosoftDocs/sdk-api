---
UID: NF:mfplay.IMFPMediaItem.GetStartStopPosition
title: IMFPMediaItem::GetStartStopPosition (mfplay.h)
description: Gets the start and stop times for the media item.
helpviewer_keywords: ["GetStartStopPosition","GetStartStopPosition method [Media Foundation]","GetStartStopPosition method [Media Foundation]","IMFPMediaItem interface","IMFPMediaItem interface [Media Foundation]","GetStartStopPosition method","IMFPMediaItem.GetStartStopPosition","IMFPMediaItem::GetStartStopPosition","mf.imfpmediaitem_getstartstopposition","mfplay/IMFPMediaItem::GetStartStopPosition"]
old-location: mf\imfpmediaitem_getstartstopposition.htm
tech.root: mf
ms.assetid: c992bbec-a5ca-4ece-a883-2a7d7b5d49b3
ms.date: 12/05/2018
ms.keywords: GetStartStopPosition, GetStartStopPosition method [Media Foundation], GetStartStopPosition method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetStartStopPosition method, IMFPMediaItem.GetStartStopPosition, IMFPMediaItem::GetStartStopPosition, mf.imfpmediaitem_getstartstopposition, mfplay/IMFPMediaItem::GetStartStopPosition
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IMFPMediaItem::GetStartStopPosition
 - mfplay/IMFPMediaItem::GetStartStopPosition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplay.h
api_name:
 - IMFPMediaItem.GetStartStopPosition
---

# IMFPMediaItem::GetStartStopPosition


## -description

<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Gets the start and stop times for the media item.

## -parameters

### -param pguidStartPositionType [out]

Receives the unit of time for the start position. See Remarks. This parameter can be <b>NULL</b>.

### -param pvStartValue [out]

Receives the start position. The meaning and data type of this parameter are indicated by the <i>pguidStartPositionType</i> parameter. The  <i>pvStartValue</i> parameter must be <b>NULL</b> if <i>pguidStartPositionType</i> is <b>NULL</b>, and cannot be <b>NULL</b> otherwise.

### -param pguidStopPositionType [out]

Receives the unit of time for the stop position. See Remarks. This parameter can be <b>NULL</b>.

### -param pvStopValue [out]

Stop position. The meaning and data type of this parameter are indicated by the <i>pguidStopPositionType</i> parameter. The <i>pvStopValue</i>  parameter must be <b>NULL</b> if <i>pguidStopPositionType</i> is <b>NULL</b>, and cannot be <b>NULL</b> otherwise.

## -returns

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -remarks

The <i>pguidStartPositionType</i> and <i>pguidStopPositionType</i> parameters receive the units of time that are used. Currently, the only supported value is <b>MFP_POSITIONTYPE_100NS</b>.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>MFP_POSITIONTYPE_100NS</td>
<td>100-nanosecond units. The time parameter (<i>pvStartValue</i> or <i>pvStopValue</i>) uses the following data type:<ul>
<li>Variant type (<b>vt</b>): VT_I8</li>
<li>Variant member: <b>hVal</b></li>
</ul>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/how-to-play-a-file-clip">How to Play a File Clip</a>



<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
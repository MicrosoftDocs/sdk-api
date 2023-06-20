---
UID: NF:contentpartner.IWMPContentPartner.StationEvent
title: IWMPContentPartner::StationEvent (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPContentPartner interface [Windows Media Player]","StationEvent method","IWMPContentPartner.StationEvent","IWMPContentPartner::StationEvent","IWMPContentPartnerStationEvent","StationEvent","StationEvent method [Windows Media Player]","StationEvent method [Windows Media Player]","IWMPContentPartner interface","contentpartner/IWMPContentPartner::StationEvent","wmp.iwmpcontentpartner_stationevent"]
old-location: wmp\iwmpcontentpartner_stationevent.htm
tech.root: WMP
ms.assetid: 0505a1e9-489f-416a-88b8-e8b76ae94b70
ms.date: 4/26/2023
ms.keywords: IWMPContentPartner interface [Windows Media Player],StationEvent method, IWMPContentPartner.StationEvent, IWMPContentPartner::StationEvent, IWMPContentPartnerStationEvent, StationEvent, StationEvent method [Windows Media Player], StationEvent method [Windows Media Player],IWMPContentPartner interface, contentpartner/IWMPContentPartner::StationEvent, wmp.iwmpcontentpartner_stationevent
req.header: contentpartner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11
req.target-min-winversvr: 
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
 - IWMPContentPartner::StationEvent
 - contentpartner/IWMPContentPartner::StationEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - contentpartner.h
api_name:
 - IWMPContentPartner.StationEvent
---

# IWMPContentPartner::StationEvent


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>StationEvent</b> method notifies the plug-in of events during playback of a Windows Media metafile playlist (ASX file).

## -parameters

### -param bstrStationEventType [in]

<b>BSTR</b> containing the event type. The caller (Windows Media Player) sets this parameter to one of the following values.

<table>
<tr>
<th>String
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>g_szStationEvent_Started</td>
<td>A track started playing.</td>
</tr>
<tr>
<td>g_szStationEvent_Complete</td>
<td>A track finished playing.</td>
</tr>
<tr>
<td>g_szStationEvent_Skipped</td>
<td>A track was skipped.</td>
</tr>
</table>

### -param StationId [in]

The station ID.

### -param PlaylistIndex [in]

The playlist index.

### -param TrackID [in]

The track ID.

### -param TrackData [in]

<b>BSTR</b> containing track data.

### -param dwSecondsPlayed [in]

Number of seconds that the playlist was played.

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

This method is called to enable logging of certain ASX events when an ASX file created by the online store is played.

## -see-also

<a href="/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>



<a href="/windows/desktop/WMP/windows-media-metafiles-overview">Windows Media Metafiles Overview</a>
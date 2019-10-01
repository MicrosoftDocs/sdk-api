---
UID: NF:contentpartner.IWMPContentPartner.StationEvent
title: IWMPContentPartner::StationEvent (contentpartner.h)
author: windows-sdk-content
description: Note  This section describes functionality designed for use by online stores.
old-location: wmp\iwmpcontentpartner_stationevent.htm
tech.root: WMP
ms.assetid: 0505a1e9-489f-416a-88b8-e8b76ae94b70
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPContentPartner interface [Windows Media Player],StationEvent method, IWMPContentPartner.StationEvent, IWMPContentPartner::StationEvent, IWMPContentPartnerStationEvent, StationEvent, StationEvent method [Windows Media Player], StationEvent method [Windows Media Player],IWMPContentPartner interface, contentpartner/IWMPContentPartner::StationEvent, wmp.iwmpcontentpartner_stationevent
ms.topic: method
f1_keywords: 
 - "contentpartner/IWMPContentPartner.StationEvent"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - contentpartner.h
api_name:
 - IWMPContentPartner.StationEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPContentPartner::StationEvent


## -description



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




<a href="https://docs.microsoft.com/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner">IWMPContentPartner Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/windows-media-metafiles-overview">Windows Media Metafiles Overview</a>
 

 


---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
<th>
                  String
                </th>
<th>
                  Description
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




<a href="https://msdn.microsoft.com/2078ebd4-3570-4c39-9081-1b55d9e8286f">IWMPContentPartner Interface</a>



<a href="https://msdn.microsoft.com/5b7742c0-f416-4bf4-ae03-9554b51fe620">Windows Media Metafiles Overview</a>
 

 


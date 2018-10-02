---
UID: NN:imapi2.IRawCDImageTrackInfo
title: IRawCDImageTrackInfo
author: windows-sdk-content
description: Use this interface to track per-track properties that are applied to CD media.
old-location: imapi\irawcdimagetrackinfo.htm
tech.root: imapi
ms.assetid: 5d074279-35fb-48d0-b298-c1a83f57d805
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IRawCDImageTrackInfo, IRawCDImageTrackInfo interface [IMAPI], IRawCDImageTrackInfo interface [IMAPI],described, imapi.irawcdimagetrackinfo, imapi2/IRawCDImageTrackInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - imapi2.h
api_name:
 - IRawCDImageTrackInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRawCDImageTrackInfo interface


## -description


Use this interface to track per-track properties that are applied to CD media.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawCDImageTrackInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IRawCDImageTrackInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRawCDImageTrackInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e322485-4542-4229-9b3e-17c9774d14b5">get_AudioHasPreemphasis</a>
</td>
<td align="left" width="63%">
Retrieves  the value that specifies if an audio track has an additional pre-emphasis added to the audio data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b9f277d-b1bb-4704-8a25-cd26fdf46069">get_DigitalAudioCopySetting</a>
</td>
<td align="left" width="63%">
Retrieves the value for the bit that represents the current digital audio copy setting on the resulting media.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e498391-37c6-4ac5-8d36-f3752ad5c4a4">get_ISRC</a>
</td>
<td align="left" width="63%">
Retrieves the International Standard Recording Code (ISRC) currently associated with the track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1762620b-b429-4674-85e2-f6f206de1a4f">get_SectorCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of user sectors in this track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbec6c4b-dd0e-46c3-9e46-97b8f98438b3">get_SectorType</a>
</td>
<td align="left" width="63%">
Retrieves the type of data provided for the sectors in this track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e1d1404-c52d-4e27-970a-bc1b59995a87">get_StartingLba</a>
</td>
<td align="left" width="63%">
Retrieves the LBA of the first user sectors in this track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a83766f7-8d02-47df-9691-26d6f2cd0d5b">get_TrackIndexes</a>
</td>
<td align="left" width="63%">
Retrieves the one-based index of the tracks on the disc.  If the  first track number is set to one, then this value is equivalent to the <b>TrackNumber</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccc84237-3819-45b4-980a-a73669f605fb">get_TrackNumber</a>
</td>
<td align="left" width="63%">
Retrieves the track number for this track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60b1d577-2eb7-4767-94ee-03df465234e9">put_AudioHasPreemphasis</a>
</td>
<td align="left" width="63%">
Sets the value that specifies if an audio track has an additional pre-emphasis added to the audio data prior to being written to CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48d00305-4dc4-432c-80b7-955bbcdb3cc2">put_DigitalAudioCopySetting</a>
</td>
<td align="left" width="63%">
Sets the digital audio copy  "Allowed" bit to one of three values on the resulting media.  Please see the <a href="https://msdn.microsoft.com/6bc38584-2e44-4c1a-b5bb-a91c0ffe7e6b">IMAPI_CD_TRACK_DIGITAL_COPY_SETTING</a> enumeration for additional information on each possible value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c94357dc-9d9f-40a7-8709-51f8d5bc09e5">put_ISRC</a>
</td>
<td align="left" width="63%">
Sets  the International Standard Recording Code (ISRC) currently associated with the track.

</td>
</tr>
</table> 


## -remarks



This interface is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/3af4a8c9-66b7-490e-aafa-fdfe614f5f3e">IMAPI_CD_SECTOR_TYPE</a>



<a href="https://msdn.microsoft.com/6bc38584-2e44-4c1a-b5bb-a91c0ffe7e6b">IMAPI_CD_TRACK_DIGITAL_COPY_SETTING</a>
 

 


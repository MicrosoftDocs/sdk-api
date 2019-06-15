---
UID: NN:imapi2.IRawCDImageTrackInfo
title: IRawCDImageTrackInfo (imapi2.h)
author: windows-sdk-content
description: Use this interface to track per-track properties that are applied to CD media.
old-location: imapi\irawcdimagetrackinfo.htm
tech.root: imapi
ms.assetid: 5d074279-35fb-48d0-b298-c1a83f57d805
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRawCDImageTrackInfo, IRawCDImageTrackInfo interface [IMAPI], IRawCDImageTrackInfo interface [IMAPI],described, imapi.irawcdimagetrackinfo, imapi2/IRawCDImageTrackInfo
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
ms.custom: 19H1
---

# IRawCDImageTrackInfo interface


## -description


Use this interface to track per-track properties that are applied to CD media.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawCDImageTrackInfo</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IRawCDImageTrackInfo</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-irawcdimagetrackinfo-get_audiohaspreemphasis">get_AudioHasPreemphasis</a>
</td>
<td align="left" width="63%">
Retrieves  the value that specifies if an audio track has an additional pre-emphasis added to the audio data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-irawcdimagetrackinfo-get_digitalaudiocopysetting">get_DigitalAudioCopySetting</a>
</td>
<td align="left" width="63%">
Retrieves the value for the bit that represents the current digital audio copy setting on the resulting media.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-irawcdimagetrackinfo-get_isrc">get_ISRC</a>
</td>
<td align="left" width="63%">
Retrieves the International Standard Recording Code (ISRC) currently associated with the track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-irawcdimagetrackinfo-get_sectorcount">get_SectorCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of user sectors in this track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-irawcdimagetrackinfo-get_sectortype">get_SectorType</a>
</td>
<td align="left" width="63%">
Retrieves the type of data provided for the sectors in this track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-irawcdimagetrackinfo-get_startinglba">get_StartingLba</a>
</td>
<td align="left" width="63%">
Retrieves the LBA of the first user sectors in this track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-irawcdimagetrackinfo-get_trackindexes">get_TrackIndexes</a>
</td>
<td align="left" width="63%">
Retrieves the one-based index of the tracks on the disc.  If the  first track number is set to one, then this value is equivalent to the <b>TrackNumber</b> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-irawcdimagetrackinfo-get_tracknumber">get_TrackNumber</a>
</td>
<td align="left" width="63%">
Retrieves the track number for this track.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-irawcdimagetrackinfo-put_audiohaspreemphasis">put_AudioHasPreemphasis</a>
</td>
<td align="left" width="63%">
Sets the value that specifies if an audio track has an additional pre-emphasis added to the audio data prior to being written to CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-irawcdimagetrackinfo-put_digitalaudiocopysetting">put_DigitalAudioCopySetting</a>
</td>
<td align="left" width="63%">
Sets the digital audio copy  "Allowed" bit to one of three values on the resulting media.  Please see the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/ne-imapi2-_imapi_cd_track_digital_copy_setting">IMAPI_CD_TRACK_DIGITAL_COPY_SETTING</a> enumeration for additional information on each possible value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-irawcdimagetrackinfo-put_isrc">put_ISRC</a>
</td>
<td align="left" width="63%">
Sets  the International Standard Recording Code (ISRC) currently associated with the track.

</td>
</tr>
</table> 


## -remarks



This interface is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/ne-imapi2-_imapi_cd_sector_type">IMAPI_CD_SECTOR_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/ne-imapi2-_imapi_cd_track_digital_copy_setting">IMAPI_CD_TRACK_DIGITAL_COPY_SETTING</a>
 

 


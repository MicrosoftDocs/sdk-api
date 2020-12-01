---
UID: NN:imapi2.IRawCDImageCreator
title: IRawCDImageCreator (imapi2.h)
description: Use this interface to create a RAW CD image for use in writing to CD media in Disc-at-Once (DAO) mode. Images created with this interface can be written to CD media using the IDiscFormat2RawCD interface.
helpviewer_keywords: ["IRawCDImageCreator","IRawCDImageCreator interface [IMAPI]","IRawCDImageCreator interface [IMAPI]","described","imapi.irawcdimagecreator","imapi2/IRawCDImageCreator"]
old-location: imapi\irawcdimagecreator.htm
tech.root: imapi
ms.assetid: b5fe1a32-545e-417d-9996-34d12862a0ea
ms.date: 12/05/2018
ms.keywords: IRawCDImageCreator, IRawCDImageCreator interface [IMAPI], IRawCDImageCreator interface [IMAPI],described, imapi.irawcdimagecreator, imapi2/IRawCDImageCreator
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRawCDImageCreator
 - imapi2/IRawCDImageCreator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IRawCDImageCreator
---

# IRawCDImageCreator interface


## -description

Use this interface to create a RAW CD image for use in writing to CD media in Disc-at-Once (DAO) mode. Images created with this interface can be written to CD media using the <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a> interface. 

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftRawCDImageCreator) for the class identifier and __uuidof(IRawCDImageCreator) for the interface identifier.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawCDImageCreator</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IRawCDImageCreator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRawCDImageCreator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-addspecialpregap">AddSpecialPregap</a>
</td>
<td align="left" width="63%">
Takes the provided <b>IStream</b> object and saves the interface pointer to be used as data for the pre-gap for track 1. This function is optional.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-addsubcoderwgenerator">AddSubcodeRWGenerator</a>
</td>
<td align="left" width="63%">
Allows the addition of custom R-W subcode, provided by the <b>IStream</b> object.  The provided interface must (when the final image is created) have a size equal to the number of sectors in the raw disc image * 96 bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-addtrack">AddTrack</a>
</td>
<td align="left" width="63%">
This routine takes the provided <b>IStream</b> object and saves the interface pointer as the next track in the image.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-createresultimage">CreateResultImage</a>
</td>
<td align="left" width="63%">
Creates the final <b>IStream</b> object based on the current settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-get_disablegaplessaudio">get_DisableGaplessAudio</a>
</td>
<td align="left" width="63%">
Retrieves the current value that specifies if "Gapless Audio" recording is disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-get_expectedtableofcontents">get_ExpectedTableOfContents</a>
</td>
<td align="left" width="63%">
Gets the SCSI-form table of contents for the resulting disc, if the image is created with no further modifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-get_lastusedusersectorinimage">get_LastUsedUserSectorInImage</a>
</td>
<td align="left" width="63%">
Retrieves the number of total used sectors on the current media, including any overhead between existing tracks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-get_mediacatalognumber">get_MediaCatalogNumber</a>
</td>
<td align="left" width="63%">
Retrieves the Media Catalog Number (MCN) for the entire audio disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-get_numberofexistingtracks">get_NumberOfExistingTracks</a>
</td>
<td align="left" width="63%">
Retrieves the number of existing audio tracks on the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-get_resultingimagetype">get_ResultingImageType</a>
</td>
<td align="left" width="63%">
Retrieves the value that specifies the type of image file that is generated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-get_startingtracknumber">get_StartingTrackNumber</a>
</td>
<td align="left" width="63%">
Retrieves the starting track number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-get_startofleadout">get_StartOfLeadout</a>
</td>
<td align="left" width="63%">
Retrieves the value that defines the LBA for the start of the Leadout.  This method can be utilized to determine if the image can be written to a piece of media by comparing it against the <b>LastPossibleStartOfLeadout</b> for the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-get_startofleadoutlimit">get_StartOfLeadoutLimit</a>
</td>
<td align="left" width="63%">
Retrieves the current <i>StartOfLeadoutLimit</i> property value. This value specifies if the resulting image is required to fit on a piece of media with a <b>StartOfLeadout</b> greater than or equal to the LBA specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-get_trackinfo">get_TrackInfo</a>
</td>
<td align="left" width="63%">
Retrieves an indexed property, which takes a LONG as the index to determine which track the user is querying.  The returned object is then queried/set for the particular per-track property of interest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-put_disablegaplessaudio">put_DisableGaplessAudio</a>
</td>
<td align="left" width="63%">
Sets the value which specifies if "Gapless Audio" recording is disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-put_mediacatalognumber">put_MediaCatalogNumber</a>
</td>
<td align="left" width="63%">
Sets the Media Catalog Number (MCN) for the entire audio disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-put_resultingimagetype">put_ResultingImageType</a>
</td>
<td align="left" width="63%">
Sets the value that specifies the type of image file that is generated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-put_startingtracknumber">put_StartingTrackNumber</a>
</td>
<td align="left" width="63%">
Sets the starting track number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-put_startofleadoutlimit">put_StartOfLeadoutLimit</a>
</td>
<td align="left" width="63%">
Sets the <i>StartOfLeadoutLimit</i> property value. This value specifies if the resulting image is required to fit on a piece of media with a <b>StartOfLeadout</b> greater than or equal to the LBA specified.

<div class="alert"><b>Note</b>  The maximum supported value for this property is 398,099, which equates to MSF 88:29:74. </div>
<div> </div>
</td>
</tr>
</table>

## -remarks

Images created with this interface can be written to persistent storage for later use, or can be provided directly to the <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a> interface for writing to CD media.

DVD media does not support this type of writing.

This interface is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/ne-imapi2-imapi_cd_sector_type">IMAPI_CD_SECTOR_TYPE</a>
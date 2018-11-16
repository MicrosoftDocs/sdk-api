---
UID: NN:imapi2.IRawCDImageCreator
title: IRawCDImageCreator
author: windows-sdk-content
description: Use this interface to create a RAW CD image for use in writing to CD media in Disc-at-Once (DAO) mode. Images created with this interface can be written to CD media using the IDiscFormat2RawCD interface.
old-location: imapi\irawcdimagecreator.htm
tech.root: imapi
ms.assetid: b5fe1a32-545e-417d-9996-34d12862a0ea
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IRawCDImageCreator, IRawCDImageCreator interface [IMAPI], IRawCDImageCreator interface [IMAPI],described, imapi.irawcdimagecreator, imapi2/IRawCDImageCreator
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IRawCDImageCreator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRawCDImageCreator interface


## -description


Use this interface to create a RAW CD image for use in writing to CD media in Disc-at-Once (DAO) mode. Images created with this interface can be written to CD media using the <a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a> interface. 

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftRawCDImageCreator) for the class identifier and __uuidof(IRawCDImageCreator) for the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawCDImageCreator</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IRawCDImageCreator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/953ac9e9-b097-4fe5-8bcf-db4f9f15816e">AddSpecialPregap</a>
</td>
<td align="left" width="63%">
Takes the provided <b>IStream</b> object and saves the interface pointer to be used as data for the pre-gap for track 1. This function is optional.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b952d31e-812e-41b0-98b0-0f9afbe4b01e">AddSubcodeRWGenerator</a>
</td>
<td align="left" width="63%">
Allows the addition of custom R-W subcode, provided by the <b>IStream</b> object.  The provided interface must (when the final image is created) have a size equal to the number of sectors in the raw disc image * 96 bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/913393e8-6d60-4b1a-b482-32225860f714">AddTrack</a>
</td>
<td align="left" width="63%">
This routine takes the provided <b>IStream</b> object and saves the interface pointer as the next track in the image.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a83293f6-d5a1-49e2-884b-2b185516109d">CreateResultImage</a>
</td>
<td align="left" width="63%">
Creates the final <b>IStream</b> object based on the current settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f3bf774-3e09-40e9-bc0b-f33bfd046a51">get_DisableGaplessAudio</a>
</td>
<td align="left" width="63%">
Retrieves the current value that specifies if "Gapless Audio" recording is disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce65b26f-9cf7-4c61-a343-975e5af17f57">get_ExpectedTableOfContents</a>
</td>
<td align="left" width="63%">
Gets the SCSI-form table of contents for the resulting disc, if the image is created with no further modifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a6b907a-2475-48c8-afd7-e212144bc165">get_LastUsedUserSectorInImage</a>
</td>
<td align="left" width="63%">
Retrieves the number of total used sectors on the current media, including any overhead between existing tracks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db6f46b7-9965-4b06-a437-bdfdac7d5efa">get_MediaCatalogNumber</a>
</td>
<td align="left" width="63%">
Retrieves the Media Catalog Number (MCN) for the entire audio disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c10053d0-d9c1-4ac0-aa38-71dacf1e4425">get_NumberOfExistingTracks</a>
</td>
<td align="left" width="63%">
Retrieves the number of existing audio tracks on the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/006486f7-f766-44a1-a088-71035567a75d">get_ResultingImageType</a>
</td>
<td align="left" width="63%">
Retrieves the value that specifies the type of image file that is generated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/307ef0b4-80b2-46c1-acca-1ce5d2222eb7">get_StartingTrackNumber</a>
</td>
<td align="left" width="63%">
Retrieves the starting track number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bf40179-31f5-453f-a989-4bcd116a45aa">get_StartOfLeadout</a>
</td>
<td align="left" width="63%">
Retrieves the value that defines the LBA for the start of the Leadout.  This method can be utilized to determine if the image can be written to a piece of media by comparing it against the <b>LastPossibleStartOfLeadout</b> for the media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07397f94-fd32-4507-89dd-53de7f25b231">get_StartOfLeadoutLimit</a>
</td>
<td align="left" width="63%">
Retrieves the current <i>StartOfLeadoutLimit</i> property value. This value specifies if the resulting image is required to fit on a piece of media with a <b>StartOfLeadout</b> greater than or equal to the LBA specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6bc12fe-9274-4339-baf5-80a80512759e">get_TrackInfo</a>
</td>
<td align="left" width="63%">
Retrieves an indexed property, which takes a LONG as the index to determine which track the user is querying.  The returned object is then queried/set for the particular per-track property of interest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9e17ed7-f51a-4b28-82db-36cad1aedd39">put_DisableGaplessAudio</a>
</td>
<td align="left" width="63%">
Sets the value which specifies if "Gapless Audio" recording is disabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ba2eaac-3bbc-4625-9c5d-1f1d23bbfa66">put_MediaCatalogNumber</a>
</td>
<td align="left" width="63%">
Sets the Media Catalog Number (MCN) for the entire audio disc.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1800717a-3b8a-45b2-849b-55c37d3b1b32">put_ResultingImageType</a>
</td>
<td align="left" width="63%">
Sets the value that specifies the type of image file that is generated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38d1319b-0350-41bf-8984-fbeb4f5f3204">put_StartingTrackNumber</a>
</td>
<td align="left" width="63%">
Sets the starting track number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3483084-8339-4fe6-abd1-832832c549f3">put_StartOfLeadoutLimit</a>
</td>
<td align="left" width="63%">
Sets the <i>StartOfLeadoutLimit</i> property value. This value specifies if the resulting image is required to fit on a piece of media with a <b>StartOfLeadout</b> greater than or equal to the LBA specified.

<div class="alert"><b>Note</b>  The maximum supported value for this property is 398,099, which equates to MSF 88:29:74. </div>
<div> </div>
</td>
</tr>
</table> 


## -remarks



Images created with this interface can be written to persistent storage for later use, or can be provided directly to the <a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a> interface for writing to CD media.

DVD media does not support this type of writing.

This interface is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/3af4a8c9-66b7-490e-aafa-fdfe614f5f3e">IMAPI_CD_SECTOR_TYPE</a>
 

 


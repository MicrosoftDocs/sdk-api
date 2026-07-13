---
UID: NF:imapi2.IDiscFormat2TrackAtOnce.get_NumberOfExistingTracks
title: IDiscFormat2TrackAtOnce::get_NumberOfExistingTracks (imapi2.h)
description: Retrieves the number of existing audio tracks on the media. (IDiscFormat2TrackAtOnce.get_NumberOfExistingTracks)
helpviewer_keywords: ["IDiscFormat2TrackAtOnce interface [IMAPI]","get_NumberOfExistingTracks method","IDiscFormat2TrackAtOnce.get_NumberOfExistingTracks","IDiscFormat2TrackAtOnce::get_NumberOfExistingTracks","get_NumberOfExistingTracks","get_NumberOfExistingTracks method [IMAPI]","get_NumberOfExistingTracks method [IMAPI]","IDiscFormat2TrackAtOnce interface","imapi.idiscformat2trackatonce_get_numberofexistingtracks","imapi2/IDiscFormat2TrackAtOnce::get_NumberOfExistingTracks"]
old-location: imapi\idiscformat2trackatonce_get_numberofexistingtracks.htm
tech.root: imapi
ms.assetid: 6a8bcfe2-d09a-4eec-8e68-5e0dfc868033
ms.date: 12/05/2018
ms.keywords: IDiscFormat2TrackAtOnce interface [IMAPI],get_NumberOfExistingTracks method, IDiscFormat2TrackAtOnce.get_NumberOfExistingTracks, IDiscFormat2TrackAtOnce::get_NumberOfExistingTracks, get_NumberOfExistingTracks, get_NumberOfExistingTracks method [IMAPI], get_NumberOfExistingTracks method [IMAPI],IDiscFormat2TrackAtOnce interface, imapi.idiscformat2trackatonce_get_numberofexistingtracks, imapi2/IDiscFormat2TrackAtOnce::get_NumberOfExistingTracks
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
 - IDiscFormat2TrackAtOnce::get_NumberOfExistingTracks
 - imapi2/IDiscFormat2TrackAtOnce::get_NumberOfExistingTracks
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
 - IDiscFormat2TrackAtOnce.get_NumberOfExistingTracks
---

# IDiscFormat2TrackAtOnce::get_NumberOfExistingTracks


## -description

Retrieves the number of existing audio tracks on the media.

## -parameters

### -param value [out]

Number of completed tracks written to disc, not including the track currently being added.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_MEDIA_IS_NOT_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
The media is not prepared (IDiscFormat2TrackAtOnce::PrepareMedia has not been called).

Value: 0xC0AA0502

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
A write operation is in progress.

Value: 0xC0AA0500

</td>
</tr>
</table>

## -remarks

The value is zero if:

<ul>
<li>The media is blank</li>
<li>You call this method outside a writing session</li>
</ul>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-addaudiotrack">IDiscFormat2TrackAtOnce::AddAudioTrack</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-preparemedia">IDiscFormat2TrackAtOnce::PrepareMedia</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-releasemedia">IDiscFormat2TrackAtOnce::ReleaseMedia</a>

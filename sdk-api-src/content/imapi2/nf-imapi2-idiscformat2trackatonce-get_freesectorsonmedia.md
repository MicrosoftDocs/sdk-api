---
UID: NF:imapi2.IDiscFormat2TrackAtOnce.get_FreeSectorsOnMedia
title: IDiscFormat2TrackAtOnce::get_FreeSectorsOnMedia (imapi2.h)
description: Retrieves the number of sectors available for adding a new track to the media.
helpviewer_keywords: ["IDiscFormat2TrackAtOnce interface [IMAPI]","get_FreeSectorsOnMedia method","IDiscFormat2TrackAtOnce.get_FreeSectorsOnMedia","IDiscFormat2TrackAtOnce::get_FreeSectorsOnMedia","get_FreeSectorsOnMedia","get_FreeSectorsOnMedia method [IMAPI]","get_FreeSectorsOnMedia method [IMAPI]","IDiscFormat2TrackAtOnce interface","imapi.idiscformat2trackatonce_get_freesectorsonmedia","imapi2/IDiscFormat2TrackAtOnce::get_FreeSectorsOnMedia"]
old-location: imapi\idiscformat2trackatonce_get_freesectorsonmedia.htm
tech.root: imapi
ms.assetid: a36dd3de-ca08-4783-beca-95813402692b
ms.date: 12/05/2018
ms.keywords: IDiscFormat2TrackAtOnce interface [IMAPI],get_FreeSectorsOnMedia method, IDiscFormat2TrackAtOnce.get_FreeSectorsOnMedia, IDiscFormat2TrackAtOnce::get_FreeSectorsOnMedia, get_FreeSectorsOnMedia, get_FreeSectorsOnMedia method [IMAPI], get_FreeSectorsOnMedia method [IMAPI],IDiscFormat2TrackAtOnce interface, imapi.idiscformat2trackatonce_get_freesectorsonmedia, imapi2/IDiscFormat2TrackAtOnce::get_FreeSectorsOnMedia
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
 - IDiscFormat2TrackAtOnce::get_FreeSectorsOnMedia
 - imapi2/IDiscFormat2TrackAtOnce::get_FreeSectorsOnMedia
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
 - IDiscFormat2TrackAtOnce.get_FreeSectorsOnMedia
---

# IDiscFormat2TrackAtOnce::get_FreeSectorsOnMedia


## -description

Retrieves the number of sectors available for adding a new track to the media.

## -parameters

### -param value [out]

Number of available sectors on the media that can be used for writing audio.

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
</table>

## -remarks

If called during an <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-addaudiotrack">AddAudioTrack</a> operation, the available sectors do not reflect the sectors used in writing the current audio track. Instead, the reported value is the number of available sectors immediately preceding the call to AddAudioTrack.

## -see-also

<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_freesectorsonmedia">IDiscFormat2Data::get_FreeSectorsOnMedia</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_totalsectorsonmedia">IDiscFormat2Data::get_TotalSectorsOnMedia</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_totalsectorsonmedia">IDiscFormat2TrackAtOnce::get_TotalSectorsOnMedia</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_usedsectorsonmedia">IDiscFormat2TrackAtOnce::get_UsedSectorsOnMedia</a>
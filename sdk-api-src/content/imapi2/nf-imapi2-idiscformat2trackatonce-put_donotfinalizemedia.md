---
UID: NF:imapi2.IDiscFormat2TrackAtOnce.put_DoNotFinalizeMedia
title: IDiscFormat2TrackAtOnce::put_DoNotFinalizeMedia (imapi2.h)
description: Determines if the media is left open for writing after writing the audio track. (Put)
helpviewer_keywords: ["IDiscFormat2TrackAtOnce interface [IMAPI]","put_DoNotFinalizeMedia method","IDiscFormat2TrackAtOnce.put_DoNotFinalizeMedia","IDiscFormat2TrackAtOnce::put_DoNotFinalizeMedia","imapi.idiscformat2trackatonce_put_donotfinalizemedia","imapi2/IDiscFormat2TrackAtOnce::put_DoNotFinalizeMedia","put_DoNotFinalizeMedia","put_DoNotFinalizeMedia method [IMAPI]","put_DoNotFinalizeMedia method [IMAPI]","IDiscFormat2TrackAtOnce interface"]
old-location: imapi\idiscformat2trackatonce_put_donotfinalizemedia.htm
tech.root: imapi
ms.assetid: ffde10f9-259a-400d-b83e-f8c81bbe8f94
ms.date: 12/05/2018
ms.keywords: IDiscFormat2TrackAtOnce interface [IMAPI],put_DoNotFinalizeMedia method, IDiscFormat2TrackAtOnce.put_DoNotFinalizeMedia, IDiscFormat2TrackAtOnce::put_DoNotFinalizeMedia, imapi.idiscformat2trackatonce_put_donotfinalizemedia, imapi2/IDiscFormat2TrackAtOnce::put_DoNotFinalizeMedia, put_DoNotFinalizeMedia, put_DoNotFinalizeMedia method [IMAPI], put_DoNotFinalizeMedia method [IMAPI],IDiscFormat2TrackAtOnce interface
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
 - IDiscFormat2TrackAtOnce::put_DoNotFinalizeMedia
 - imapi2/IDiscFormat2TrackAtOnce::put_DoNotFinalizeMedia
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
 - IDiscFormat2TrackAtOnce.put_DoNotFinalizeMedia
---

# IDiscFormat2TrackAtOnce::put_DoNotFinalizeMedia


## -description

Determines if the media is left open for writing after writing the audio track.

## -parameters

### -param value [in]

Set to VARIANT_TRUE to leave the media open for writing after writing the audio track; otherwise, VARIANT_FALSE. The default is VARIANT_FALSE.

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
<dt><b>E_IMAPI_DF2TAO_WRITE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
A write operation is in progress.

Value: 0xC0AA0500

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_MEDIA_IS_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
The requested operation is not valid when media has been "prepared" but not released.

Value: 0xC0AA0503

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2TAO_PROPERTY_FOR_BLANK_MEDIA_ONLY</b></dt>
</dl>
</td>
<td width="60%">
The property cannot be changed once the media has been written to.

Value: 0xC0AA0504

</td>
</tr>
</table>

## -remarks

You can set this property before calling the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-preparemedia">IDiscFormat2TrackAtOnce::PrepareMedia</a> method or after calling the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-releasemedia">IDiscFormat2TrackAtOnce::ReleaseMedia</a> method; you cannot set it during a track-writing session. 

This property is useful to create a multi-session CD with audio in the first session and data in the second session.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-preparemedia">IDiscFormat2TrackAtOnce::PrepareMedia</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-releasemedia">IDiscFormat2TrackAtOnce::ReleaseMedia</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_donotfinalizemedia">IDiscFormat2TrackAtOnce::get_DoNotFinalizeMedia</a>

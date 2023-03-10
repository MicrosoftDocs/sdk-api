---
UID: NF:imapi2.IDiscFormat2TrackAtOnce.CancelAddTrack
title: IDiscFormat2TrackAtOnce::CancelAddTrack (imapi2.h)
description: Cancels the current write operation. (IDiscFormat2TrackAtOnce.CancelAddTrack)
helpviewer_keywords: ["CancelAddTrack","CancelAddTrack method [IMAPI]","CancelAddTrack method [IMAPI]","IDiscFormat2TrackAtOnce interface","IDiscFormat2TrackAtOnce interface [IMAPI]","CancelAddTrack method","IDiscFormat2TrackAtOnce.CancelAddTrack","IDiscFormat2TrackAtOnce::CancelAddTrack","imapi.idiscformat2trackatonce_canceladdtrack","imapi2/IDiscFormat2TrackAtOnce::CancelAddTrack"]
old-location: imapi\idiscformat2trackatonce_canceladdtrack.htm
tech.root: imapi
ms.assetid: 09e71d36-da1d-4ba0-bd6b-4ce4425d481a
ms.date: 12/05/2018
ms.keywords: CancelAddTrack, CancelAddTrack method [IMAPI], CancelAddTrack method [IMAPI],IDiscFormat2TrackAtOnce interface, IDiscFormat2TrackAtOnce interface [IMAPI],CancelAddTrack method, IDiscFormat2TrackAtOnce.CancelAddTrack, IDiscFormat2TrackAtOnce::CancelAddTrack, imapi.idiscformat2trackatonce_canceladdtrack, imapi2/IDiscFormat2TrackAtOnce::CancelAddTrack
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
 - IDiscFormat2TrackAtOnce::CancelAddTrack
 - imapi2/IDiscFormat2TrackAtOnce::CancelAddTrack
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
 - IDiscFormat2TrackAtOnce.CancelAddTrack
---

# IDiscFormat2TrackAtOnce::CancelAddTrack


## -description

Cancels the current write operation.



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
<dt><b>E_IMAPI_DF2TAO_WRITE_NOT_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
There is no write operation currently in progress.

Value: 0xC0AA0501

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified failure.

Value: 0x80004005

</td>
</tr>
</table>

## -remarks

To cancel the write operation, you must call this method from the <a href="/windows/desktop/api/imapi2/nf-imapi2-ddiscformat2trackatonceevents-update">DDiscFormat2TrackAtOnceEvents::Update</a> event handler that you implemented. 

You must also call the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-releasemedia">IDiscFormat2TrackAtOnce::ReleaseMedia</a> method after calling this method.

Note that calling this method does not immediately cancel the write operation on all media due to media-specific requirements. For example, when writing to a CD, the write operation can continue for up to three more minutes.

This method may result in a partial audio track having already been recorded.  The method will attempt to keep the media in a usable state and will simply treat the canceled track as being shorter than originally described by the <b>IStream</b>.  Callers should query the number of tracks and track sizes after canceling to determine the disc state.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-addaudiotrack">IDiscFormat2TrackAtOnce::AddAudioTrack</a>

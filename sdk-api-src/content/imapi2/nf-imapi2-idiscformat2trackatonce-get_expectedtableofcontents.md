---
UID: NF:imapi2.IDiscFormat2TrackAtOnce.get_ExpectedTableOfContents
title: IDiscFormat2TrackAtOnce::get_ExpectedTableOfContents (imapi2.h)
description: Retrieves the table of content for the audio tracks that were laid on the media within the track-writing session.
helpviewer_keywords: ["IDiscFormat2TrackAtOnce interface [IMAPI]","get_ExpectedTableOfContents method","IDiscFormat2TrackAtOnce.get_ExpectedTableOfContents","IDiscFormat2TrackAtOnce::get_ExpectedTableOfContents","get_ExpectedTableOfContents","get_ExpectedTableOfContents method [IMAPI]","get_ExpectedTableOfContents method [IMAPI]","IDiscFormat2TrackAtOnce interface","imapi.idiscformat2trackatonce_get_expectedtableofcontents","imapi2/IDiscFormat2TrackAtOnce::get_ExpectedTableOfContents"]
old-location: imapi\idiscformat2trackatonce_get_expectedtableofcontents.htm
tech.root: imapi
ms.assetid: b414bdbc-0f49-4a00-9b25-fa738f5f880b
ms.date: 12/05/2018
ms.keywords: IDiscFormat2TrackAtOnce interface [IMAPI],get_ExpectedTableOfContents method, IDiscFormat2TrackAtOnce.get_ExpectedTableOfContents, IDiscFormat2TrackAtOnce::get_ExpectedTableOfContents, get_ExpectedTableOfContents, get_ExpectedTableOfContents method [IMAPI], get_ExpectedTableOfContents method [IMAPI],IDiscFormat2TrackAtOnce interface, imapi.idiscformat2trackatonce_get_expectedtableofcontents, imapi2/IDiscFormat2TrackAtOnce::get_ExpectedTableOfContents
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
 - IDiscFormat2TrackAtOnce::get_ExpectedTableOfContents
 - imapi2/IDiscFormat2TrackAtOnce::get_ExpectedTableOfContents
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
 - IDiscFormat2TrackAtOnce.get_ExpectedTableOfContents
---

# IDiscFormat2TrackAtOnce::get_ExpectedTableOfContents


## -description

Retrieves the table of content for the audio tracks that were laid on the media within the track-writing session.

## -parameters

### -param value [out]

Table of contents for the audio tracks that were laid on the media within the track-writing session. Each element of the list is a <b>VARIANT</b> of type <b>VT_BYREF|VT_UI1</b>. The <b>pbVal</b> member of the variant contains a binary blob. For details of the blob, see the READ TOC command at ftp://ftp.t10.org/t10/drafts/mmc5/mmc5r03.pdf.

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
<dt><b>E_IMAPI_DF2TAO_TABLE_OF_CONTENTS_EMPTY_DISC</b></dt>
</dl>
</td>
<td width="60%">
The media is blank.

Value: 0xC0AA0505

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
</table>

## -remarks

The property is not accessible outside a track-writing session. Nor is the property accessible if the disc is blank.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-preparemedia">IDiscFormat2TrackAtOnce::PrepareMedia</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-releasemedia">IDiscFormat2TrackAtOnce::ReleaseMedia</a>
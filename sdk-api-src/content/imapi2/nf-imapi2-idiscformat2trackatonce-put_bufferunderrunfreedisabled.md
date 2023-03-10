---
UID: NF:imapi2.IDiscFormat2TrackAtOnce.put_BufferUnderrunFreeDisabled
title: IDiscFormat2TrackAtOnce::put_BufferUnderrunFreeDisabled (imapi2.h)
description: Determines if Buffer Underrun Free Recording is enabled.
helpviewer_keywords: ["IDiscFormat2TrackAtOnce interface [IMAPI]","put_BufferUnderrunFreeDisabled method","IDiscFormat2TrackAtOnce.put_BufferUnderrunFreeDisabled","IDiscFormat2TrackAtOnce::put_BufferUnderrunFreeDisabled","imapi.idiscformat2trackatonce_put_bufferunderrunfreedisabled","imapi2/IDiscFormat2TrackAtOnce::put_BufferUnderrunFreeDisabled","put_BufferUnderrunFreeDisabled","put_BufferUnderrunFreeDisabled method [IMAPI]","put_BufferUnderrunFreeDisabled method [IMAPI]","IDiscFormat2TrackAtOnce interface"]
old-location: imapi\idiscformat2trackatonce_put_bufferunderrunfreedisabled.htm
tech.root: imapi
ms.assetid: 93a19bd7-9302-49f5-a5e5-573bf72725a3
ms.date: 12/05/2018
ms.keywords: IDiscFormat2TrackAtOnce interface [IMAPI],put_BufferUnderrunFreeDisabled method, IDiscFormat2TrackAtOnce.put_BufferUnderrunFreeDisabled, IDiscFormat2TrackAtOnce::put_BufferUnderrunFreeDisabled, imapi.idiscformat2trackatonce_put_bufferunderrunfreedisabled, imapi2/IDiscFormat2TrackAtOnce::put_BufferUnderrunFreeDisabled, put_BufferUnderrunFreeDisabled, put_BufferUnderrunFreeDisabled method [IMAPI], put_BufferUnderrunFreeDisabled method [IMAPI],IDiscFormat2TrackAtOnce interface
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
 - IDiscFormat2TrackAtOnce::put_BufferUnderrunFreeDisabled
 - imapi2/IDiscFormat2TrackAtOnce::put_BufferUnderrunFreeDisabled
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
 - IDiscFormat2TrackAtOnce.put_BufferUnderrunFreeDisabled
---

# IDiscFormat2TrackAtOnce::put_BufferUnderrunFreeDisabled


## -description

Determines if Buffer Underrun Free Recording is enabled.

## -parameters

### -param value [in]

Set to VARIANT_TRUE to disable Buffer Underrun Free Recording; otherwise, VARIANT_FALSE. The default is VARIANT_FALSE (enabled).

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

Buffer underrun can be an issue if the data stream does not enter the buffer fast enough to keep the device continuously writing. In turn, the stop and start action of writing can cause data on the disc to be unusable. Buffer Underrun Free (BUF) recording allows the laser to start and stop without damaging data already written to the disc. Disabling of BUF recording is possible only on CD-R/RW media.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_bufferunderrunfreedisabled">IDiscFormat2TrackAtOnce::get_BufferUnderrunFreeDisabled</a>
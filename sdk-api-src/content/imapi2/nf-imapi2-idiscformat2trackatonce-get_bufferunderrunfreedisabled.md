---
UID: NF:imapi2.IDiscFormat2TrackAtOnce.get_BufferUnderrunFreeDisabled
title: IDiscFormat2TrackAtOnce::get_BufferUnderrunFreeDisabled (imapi2.h)
description: Determines if Buffer Underrun Free recording is enabled. (IDiscFormat2TrackAtOnce.get_BufferUnderrunFreeDisabled)
helpviewer_keywords: ["IDiscFormat2TrackAtOnce interface [IMAPI]","get_BufferUnderrunFreeDisabled method","IDiscFormat2TrackAtOnce.get_BufferUnderrunFreeDisabled","IDiscFormat2TrackAtOnce::get_BufferUnderrunFreeDisabled","get_BufferUnderrunFreeDisabled","get_BufferUnderrunFreeDisabled method [IMAPI]","get_BufferUnderrunFreeDisabled method [IMAPI]","IDiscFormat2TrackAtOnce interface","imapi.idiscformat2trackatonce_get_bufferunderrunfreedisabled","imapi2/IDiscFormat2TrackAtOnce::get_BufferUnderrunFreeDisabled"]
old-location: imapi\idiscformat2trackatonce_get_bufferunderrunfreedisabled.htm
tech.root: imapi
ms.assetid: 8223c46b-b754-47a1-aab9-0ebb949e79f8
ms.date: 12/05/2018
ms.keywords: IDiscFormat2TrackAtOnce interface [IMAPI],get_BufferUnderrunFreeDisabled method, IDiscFormat2TrackAtOnce.get_BufferUnderrunFreeDisabled, IDiscFormat2TrackAtOnce::get_BufferUnderrunFreeDisabled, get_BufferUnderrunFreeDisabled, get_BufferUnderrunFreeDisabled method [IMAPI], get_BufferUnderrunFreeDisabled method [IMAPI],IDiscFormat2TrackAtOnce interface, imapi.idiscformat2trackatonce_get_bufferunderrunfreedisabled, imapi2/IDiscFormat2TrackAtOnce::get_BufferUnderrunFreeDisabled
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
 - IDiscFormat2TrackAtOnce::get_BufferUnderrunFreeDisabled
 - imapi2/IDiscFormat2TrackAtOnce::get_BufferUnderrunFreeDisabled
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
 - IDiscFormat2TrackAtOnce.get_BufferUnderrunFreeDisabled
---

# IDiscFormat2TrackAtOnce::get_BufferUnderrunFreeDisabled


## -description

Determines if Buffer Underrun Free recording is enabled.

## -parameters

### -param value [out]

Is VARIANT_TRUE if Buffer Underrun Free recording is disabled; otherwise, VARIANT_FALSE (enabled).

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
</table>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-put_bufferunderrunfreedisabled">IDiscFormat2TrackAtOnce::put_BufferUnderrunFreeDisabled</a>

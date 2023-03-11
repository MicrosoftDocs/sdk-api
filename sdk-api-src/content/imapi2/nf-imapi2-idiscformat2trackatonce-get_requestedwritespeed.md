---
UID: NF:imapi2.IDiscFormat2TrackAtOnce.get_RequestedWriteSpeed
title: IDiscFormat2TrackAtOnce::get_RequestedWriteSpeed (imapi2.h)
description: Retrieves the requested write speed. (IDiscFormat2TrackAtOnce.get_RequestedWriteSpeed)
helpviewer_keywords: ["IDiscFormat2TrackAtOnce interface [IMAPI]","get_RequestedWriteSpeed method","IDiscFormat2TrackAtOnce.get_RequestedWriteSpeed","IDiscFormat2TrackAtOnce::get_RequestedWriteSpeed","get_RequestedWriteSpeed","get_RequestedWriteSpeed method [IMAPI]","get_RequestedWriteSpeed method [IMAPI]","IDiscFormat2TrackAtOnce interface","imapi.idiscformat2trackatonce_get_requestedwritespeed","imapi2/IDiscFormat2TrackAtOnce::get_RequestedWriteSpeed"]
old-location: imapi\idiscformat2trackatonce_get_requestedwritespeed.htm
tech.root: imapi
ms.assetid: 8fe83f25-9d7d-472d-9b84-90e00c0b5a51
ms.date: 12/05/2018
ms.keywords: IDiscFormat2TrackAtOnce interface [IMAPI],get_RequestedWriteSpeed method, IDiscFormat2TrackAtOnce.get_RequestedWriteSpeed, IDiscFormat2TrackAtOnce::get_RequestedWriteSpeed, get_RequestedWriteSpeed, get_RequestedWriteSpeed method [IMAPI], get_RequestedWriteSpeed method [IMAPI],IDiscFormat2TrackAtOnce interface, imapi.idiscformat2trackatonce_get_requestedwritespeed, imapi2/IDiscFormat2TrackAtOnce::get_RequestedWriteSpeed
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
 - IDiscFormat2TrackAtOnce::get_RequestedWriteSpeed
 - imapi2/IDiscFormat2TrackAtOnce::get_RequestedWriteSpeed
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
 - IDiscFormat2TrackAtOnce.get_RequestedWriteSpeed
---

# IDiscFormat2TrackAtOnce::get_RequestedWriteSpeed


## -description

Retrieves the requested write speed.

## -parameters

### -param value [out]

Requested write speed measured in disc sectors per second.

A value of 0xFFFFFFFF (-1) requests that the write occurs using the fastest supported speed for the media.

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

## -remarks

This is the value specified in the most recent call to the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-setwritespeed">IDiscFormat2TrackAtOnce::SetWriteSpeed</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce">IDiscFormat2TrackAtOnce</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-setwritespeed">IDiscFormat2TrackAtOnce::SetWriteSpeed</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_currentwritespeed">IDiscFormat2TrackAtOnce::get_CurrentWriteSpeed</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2trackatonce-get_supportedwritespeeds">IDiscFormat2TrackAtOnce::get_SupportedWriteSpeeds</a>

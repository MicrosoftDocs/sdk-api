---
UID: NF:imapi2.IDiscFormat2RawCD.get_RequestedWriteSpeed
title: IDiscFormat2RawCD::get_RequestedWriteSpeed (imapi2.h)
description: Retrieves the requested write speed. (IDiscFormat2RawCD.get_RequestedWriteSpeed)
helpviewer_keywords: ["IDiscFormat2RawCD interface [IMAPI]","get_RequestedWriteSpeed method","IDiscFormat2RawCD.get_RequestedWriteSpeed","IDiscFormat2RawCD::get_RequestedWriteSpeed","get_RequestedWriteSpeed","get_RequestedWriteSpeed method [IMAPI]","get_RequestedWriteSpeed method [IMAPI]","IDiscFormat2RawCD interface","imapi.idiscformat2rawcd_get_requestedwritespeed","imapi2/IDiscFormat2RawCD::get_RequestedWriteSpeed"]
old-location: imapi\idiscformat2rawcd_get_requestedwritespeed.htm
tech.root: imapi
ms.assetid: 0b718fe5-197e-4dc7-a8df-f2febf76aaab
ms.date: 12/05/2018
ms.keywords: IDiscFormat2RawCD interface [IMAPI],get_RequestedWriteSpeed method, IDiscFormat2RawCD.get_RequestedWriteSpeed, IDiscFormat2RawCD::get_RequestedWriteSpeed, get_RequestedWriteSpeed, get_RequestedWriteSpeed method [IMAPI], get_RequestedWriteSpeed method [IMAPI],IDiscFormat2RawCD interface, imapi.idiscformat2rawcd_get_requestedwritespeed, imapi2/IDiscFormat2RawCD::get_RequestedWriteSpeed
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
 - IDiscFormat2RawCD::get_RequestedWriteSpeed
 - imapi2/IDiscFormat2RawCD::get_RequestedWriteSpeed
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
 - IDiscFormat2RawCD.get_RequestedWriteSpeed
---

# IDiscFormat2RawCD::get_RequestedWriteSpeed


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

This is the value specified in the most recent call to the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-setwritespeed">IDiscFormat2RawCD::SetWriteSpeed</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-setwritespeed">IDiscFormat2RawCD::SetWriteSpeed</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_currentwritespeed">IDiscFormat2RawCD::get_CurrentWriteSpeed</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_supportedwritespeeds">IDiscFormat2RawCD::get_SupportedWriteSpeeds</a>

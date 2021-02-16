---
UID: NF:imapi2.IDiscFormat2RawCD.get_RequestedSectorType
title: IDiscFormat2RawCD::get_RequestedSectorType (imapi2.h)
description: Retrieves the requested data sector to use during write of the stream.
helpviewer_keywords: ["IDiscFormat2RawCD interface [IMAPI]","get_RequestedSectorType method","IDiscFormat2RawCD.get_RequestedSectorType","IDiscFormat2RawCD::get_RequestedSectorType","get_RequestedSectorType","get_RequestedSectorType method [IMAPI]","get_RequestedSectorType method [IMAPI]","IDiscFormat2RawCD interface","imapi.idiscformat2rawcd__get_requestedsectortype_","imapi2/IDiscFormat2RawCD::get_RequestedSectorType"]
old-location: imapi\idiscformat2rawcd__get_requestedsectortype_.htm
tech.root: imapi
ms.assetid: 7964e25e-43ed-4ed0-aeee-dac656700fea
ms.date: 12/05/2018
ms.keywords: IDiscFormat2RawCD interface [IMAPI],get_RequestedSectorType method, IDiscFormat2RawCD.get_RequestedSectorType, IDiscFormat2RawCD::get_RequestedSectorType, get_RequestedSectorType, get_RequestedSectorType method [IMAPI], get_RequestedSectorType method [IMAPI],IDiscFormat2RawCD interface, imapi.idiscformat2rawcd__get_requestedsectortype_, imapi2/IDiscFormat2RawCD::get_RequestedSectorType
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
 - IDiscFormat2RawCD::get_RequestedSectorType
 - imapi2/IDiscFormat2RawCD::get_RequestedSectorType
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
 - IDiscFormat2RawCD.get_RequestedSectorType
---

# IDiscFormat2RawCD::get_RequestedSectorType


## -description

Retrieves the requested data sector to use during write of the stream.

## -parameters

### -param value [out]

Requested data sector type. For possible values, see <a href="/windows/win32/api/imapi2/ne-imapi2-imapi_format2_raw_cd_data_sector_type">IMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE</a>.

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
<dt><b>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
The requested operation is only valid when media has been "prepared".

Value: 0xC0AA0602

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_supportedsectortypes">IDiscFormat2RawCD::get_SupportedSectorTypes</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-put_requestedsectortype">IDiscFormat2RawCD::put_RequestedSectorType</a>
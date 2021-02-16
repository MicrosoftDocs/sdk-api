---
UID: NF:imapi2.IDiscFormat2RawCD.put_RequestedSectorType
title: IDiscFormat2RawCD::put_RequestedSectorType (imapi2.h)
description: Sets the requested data sector to use for writing the stream.
helpviewer_keywords: ["IDiscFormat2RawCD interface [IMAPI]","put_RequestedSectorType method","IDiscFormat2RawCD.put_RequestedSectorType","IDiscFormat2RawCD::put_RequestedSectorType","imapi.idiscformat2rawcd__put_requestedsectortype_","imapi2/IDiscFormat2RawCD::put_RequestedSectorType","put_RequestedSectorType","put_RequestedSectorType method [IMAPI]","put_RequestedSectorType method [IMAPI]","IDiscFormat2RawCD interface"]
old-location: imapi\idiscformat2rawcd__put_requestedsectortype_.htm
tech.root: imapi
ms.assetid: fd9d7e1d-5672-482f-ac83-efcab3adbac4
ms.date: 12/05/2018
ms.keywords: IDiscFormat2RawCD interface [IMAPI],put_RequestedSectorType method, IDiscFormat2RawCD.put_RequestedSectorType, IDiscFormat2RawCD::put_RequestedSectorType, imapi.idiscformat2rawcd__put_requestedsectortype_, imapi2/IDiscFormat2RawCD::put_RequestedSectorType, put_RequestedSectorType, put_RequestedSectorType method [IMAPI], put_RequestedSectorType method [IMAPI],IDiscFormat2RawCD interface
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
 - IDiscFormat2RawCD::put_RequestedSectorType
 - imapi2/IDiscFormat2RawCD::put_RequestedSectorType
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
 - IDiscFormat2RawCD.put_RequestedSectorType
---

# IDiscFormat2RawCD::put_RequestedSectorType


## -description

Sets the requested data sector to use for writing the stream.

## -parameters

### -param value [in]

Data sector to use for writing the stream. For possible values, see the <a href="/windows/win32/api/imapi2/ne-imapi2-imapi_format2_raw_cd_data_sector_type">IMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE</a> enumeration type. The default is <b>IMAPI_FORMAT2_RAW_CD_SUBCODE_IS_COOKED</b>.

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
<dt><b>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
There is currently a write operation in progress.

Value: 0xC0AA0600

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
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2RAW_DATA_BLOCK_TYPE_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The requested data block type is not supported by the current device.

Value: 0xC0AA060E

</td>
</tr>
</table>

## -remarks

For a list of supported data sector types, call the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_supportedsectortypes">IDiscFormat2RawCD::get_SupportedSectorTypes</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_requestedsectortype">IDiscFormat2RawCD::get_RequestedSectorType</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-get_supportedsectortypes">IDiscFormat2RawCD::get_SupportedSectorTypes</a>
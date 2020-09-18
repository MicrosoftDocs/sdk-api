---
UID: NF:imapi2.IDiscFormat2RawCD.get_StartOfNextSession
title: IDiscFormat2RawCD::get_StartOfNextSession (imapi2.h)
description: Retrieves the first sector of the next session.
helpviewer_keywords: ["IDiscFormat2RawCD interface [IMAPI]","get_StartOfNextSession method","IDiscFormat2RawCD.get_StartOfNextSession","IDiscFormat2RawCD::get_StartOfNextSession","get_StartOfNextSession","get_StartOfNextSession method [IMAPI]","get_StartOfNextSession method [IMAPI]","IDiscFormat2RawCD interface","imapi.idiscformat2rawcd_get_startofnextsession","imapi2/IDiscFormat2RawCD::get_StartOfNextSession"]
old-location: imapi\idiscformat2rawcd_get_startofnextsession.htm
tech.root: imapi
ms.assetid: d9ffe037-c7a6-40c2-a809-58dbfd9e7415
ms.date: 12/05/2018
ms.keywords: IDiscFormat2RawCD interface [IMAPI],get_StartOfNextSession method, IDiscFormat2RawCD.get_StartOfNextSession, IDiscFormat2RawCD::get_StartOfNextSession, get_StartOfNextSession, get_StartOfNextSession method [IMAPI], get_StartOfNextSession method [IMAPI],IDiscFormat2RawCD interface, imapi.idiscformat2rawcd_get_startofnextsession, imapi2/IDiscFormat2RawCD::get_StartOfNextSession
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
 - IDiscFormat2RawCD::get_StartOfNextSession
 - imapi2/IDiscFormat2RawCD::get_StartOfNextSession
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
 - IDiscFormat2RawCD.get_StartOfNextSession
---

# IDiscFormat2RawCD::get_StartOfNextSession


## -description

Retrieves the first sector of the next session.

## -parameters

### -param value [out]

Sector number for the start of the next write operation.  This value can be negative for blank media.

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

## -remarks

The client application that creates an image must provide appropriately sized lead-in and lead-out data. The application developer using the <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a> interface must understand the formats of lead-in and lead-out for the first and subsequent sessions. Note that lead-in LBA for the first session is negative.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a>
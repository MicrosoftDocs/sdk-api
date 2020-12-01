---
UID: NF:imapi2.IDiscFormat2.IsRecorderSupported
title: IDiscFormat2::IsRecorderSupported (imapi2.h)
description: Determines if the recorder supports the given format.
helpviewer_keywords: ["IDiscFormat2 interface [IMAPI]","IsRecorderSupported method","IDiscFormat2.IsRecorderSupported","IDiscFormat2::IsRecorderSupported","IsRecorderSupported","IsRecorderSupported method [IMAPI]","IsRecorderSupported method [IMAPI]","IDiscFormat2 interface","imapi.idiscformat2_isrecordersupported","imapi2/IDiscFormat2::IsRecorderSupported"]
old-location: imapi\idiscformat2_isrecordersupported.htm
tech.root: imapi
ms.assetid: 1a96283a-a5a3-434a-834a-d539160cfc5c
ms.date: 12/05/2018
ms.keywords: IDiscFormat2 interface [IMAPI],IsRecorderSupported method, IDiscFormat2.IsRecorderSupported, IDiscFormat2::IsRecorderSupported, IsRecorderSupported, IsRecorderSupported method [IMAPI], IsRecorderSupported method [IMAPI],IDiscFormat2 interface, imapi.idiscformat2_isrecordersupported, imapi2/IDiscFormat2::IsRecorderSupported
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
 - IDiscFormat2::IsRecorderSupported
 - imapi2/IDiscFormat2::IsRecorderSupported
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
 - IDiscFormat2.IsRecorderSupported
---

# IDiscFormat2::IsRecorderSupported


## -description

Determines if the recorder supports the given format.

## -parameters

### -param recorder [in]

An <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a> interface of the recorder to test.

### -param value [out]

Is VARIANT_TRUE if the recorder supports the given format; otherwise, VARIANT_FALSE.

## -returns

S_OK or S_FALSE are returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

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

When implemented by the <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a> interface, this method will return  E_IMAPI_DF2RAW_MEDIA_IS_NOT_SUPPORTED in the event the recorder does not support the given format. It is important to note that in this specific scenario the value does not indicate that an error has occurred, but rather the result of a successful operation.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>
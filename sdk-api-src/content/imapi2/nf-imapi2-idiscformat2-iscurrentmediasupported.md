---
UID: NF:imapi2.IDiscFormat2.IsCurrentMediaSupported
title: IDiscFormat2::IsCurrentMediaSupported (imapi2.h)
description: Determines if the current media in a supported recorder supports the given format.
helpviewer_keywords: ["IDiscFormat2 interface [IMAPI]","IsCurrentMediaSupported method","IDiscFormat2.IsCurrentMediaSupported","IDiscFormat2::IsCurrentMediaSupported","IsCurrentMediaSupported","IsCurrentMediaSupported method [IMAPI]","IsCurrentMediaSupported method [IMAPI]","IDiscFormat2 interface","imapi.idiscformat2_iscurrentmediasupported","imapi2/IDiscFormat2::IsCurrentMediaSupported"]
old-location: imapi\idiscformat2_iscurrentmediasupported.htm
tech.root: imapi
ms.assetid: 2b4e8088-481e-4ff9-ba6d-aeca26287382
ms.date: 12/05/2018
ms.keywords: IDiscFormat2 interface [IMAPI],IsCurrentMediaSupported method, IDiscFormat2.IsCurrentMediaSupported, IDiscFormat2::IsCurrentMediaSupported, IsCurrentMediaSupported, IsCurrentMediaSupported method [IMAPI], IsCurrentMediaSupported method [IMAPI],IDiscFormat2 interface, imapi.idiscformat2_iscurrentmediasupported, imapi2/IDiscFormat2::IsCurrentMediaSupported
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
 - IDiscFormat2::IsCurrentMediaSupported
 - imapi2/IDiscFormat2::IsCurrentMediaSupported
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
 - IDiscFormat2.IsCurrentMediaSupported
---

# IDiscFormat2::IsCurrentMediaSupported


## -description

Determines if the current media in a supported recorder supports the given format.

## -parameters

### -param recorder [in]

An <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a> interface of the recorder to test.

### -param value [out]

Is VARIANT_TRUE if the media in the recorder supports the given format; otherwise, VARIANT_FALSE.

<div class="alert"><b>Note</b>  VARIANT_TRUE also implies that the result from <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-isrecordersupported">IsDiscRecorderSupported</a> is VARIANT_TRUE. </div>
<div> </div>

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
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_RECORDER_MEDIA_NO_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
There is no media in the device.

(HRESULT)0xC0AA0202

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Currently, Windows Vista will return<b> S_OK</b> and <b>VARIANT_FALSE</b> when media is not present in the device, while <b> E_IMAPI_RECORDER_MEDIA_NO_MEDIA</b> and <b>VARIANT_FALSE</b> are returned in Windows 7.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-isrecordersupported">IDiscFormat2::IsDiscRecorderSupported</a>
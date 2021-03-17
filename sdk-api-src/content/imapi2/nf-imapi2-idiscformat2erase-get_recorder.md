---
UID: NF:imapi2.IDiscFormat2Erase.get_Recorder
title: IDiscFormat2Erase::get_Recorder (imapi2.h)
description: Retrieves the recording device to use in the erase operation.
helpviewer_keywords: ["IDiscFormat2Erase interface [IMAPI]","get_Recorder method","IDiscFormat2Erase.get_Recorder","IDiscFormat2Erase::get_Recorder","get_Recorder","get_Recorder method [IMAPI]","get_Recorder method [IMAPI]","IDiscFormat2Erase interface","imapi.idiscformat2erase_get_recorder","imapi2/IDiscFormat2Erase::get_Recorder"]
old-location: imapi\idiscformat2erase_get_recorder.htm
tech.root: imapi
ms.assetid: 5f41ea99-e467-45ef-8f78-8b0637adf5be
ms.date: 12/05/2018
ms.keywords: IDiscFormat2Erase interface [IMAPI],get_Recorder method, IDiscFormat2Erase.get_Recorder, IDiscFormat2Erase::get_Recorder, get_Recorder, get_Recorder method [IMAPI], get_Recorder method [IMAPI],IDiscFormat2Erase interface, imapi.idiscformat2erase_get_recorder, imapi2/IDiscFormat2Erase::get_Recorder
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
 - IDiscFormat2Erase::get_Recorder
 - imapi2/IDiscFormat2Erase::get_Recorder
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
 - IDiscFormat2Erase.get_Recorder
---

# IDiscFormat2Erase::get_Recorder


## -description

Retrieves the recording device to use in the erase operation.

## -parameters

### -param value [out]

An <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a> interface that identifies the recording device to use in the erase operation.

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

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase">IDiscFormat2Erase</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2erase-put_recorder">IDiscFormat2Erase::put_Recorder</a>
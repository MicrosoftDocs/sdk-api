---
UID: NF:imapi2.IDiscFormat2DataEventArgs.get_RemainingTime
title: IDiscFormat2DataEventArgs::get_RemainingTime (imapi2.h)
description: Retrieves the estimated remaining time of the write operation. (IDiscFormat2DataEventArgs.get_RemainingTime)
helpviewer_keywords: ["IDiscFormat2DataEventArgs interface [IMAPI]","get_RemainingTime method","IDiscFormat2DataEventArgs.get_RemainingTime","IDiscFormat2DataEventArgs::get_RemainingTime","get_RemainingTime","get_RemainingTime method [IMAPI]","get_RemainingTime method [IMAPI]","IDiscFormat2DataEventArgs interface","imapi.idiscformat2dataeventargs_get_remainingtime","imapi2/IDiscFormat2DataEventArgs::get_RemainingTime"]
old-location: imapi\idiscformat2dataeventargs_get_remainingtime.htm
tech.root: imapi
ms.assetid: 1fc41d22-c85b-47dc-8d09-a8d135cfe95e
ms.date: 12/05/2018
ms.keywords: IDiscFormat2DataEventArgs interface [IMAPI],get_RemainingTime method, IDiscFormat2DataEventArgs.get_RemainingTime, IDiscFormat2DataEventArgs::get_RemainingTime, get_RemainingTime, get_RemainingTime method [IMAPI], get_RemainingTime method [IMAPI],IDiscFormat2DataEventArgs interface, imapi.idiscformat2dataeventargs_get_remainingtime, imapi2/IDiscFormat2DataEventArgs::get_RemainingTime
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
 - IDiscFormat2DataEventArgs::get_RemainingTime
 - imapi2/IDiscFormat2DataEventArgs::get_RemainingTime
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
 - IDiscFormat2DataEventArgs.get_RemainingTime
---

# IDiscFormat2DataEventArgs::get_RemainingTime


## -description

Retrieves the estimated remaining time of the write operation.

## -parameters

### -param value [out]

Estimated time, in seconds, needed for the remainder of the write operation.

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

The estimate for a single write operation can vary as the operation progresses. The drive provides updated information that can affect the projected duration of the write operation.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents">DDiscFormat2DataEvents</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs">IDiscFormat2DataEventArgs</a>

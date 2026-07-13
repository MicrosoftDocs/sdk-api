---
UID: NF:imapi2.IDiscFormat2RawCDEventArgs.get_ElapsedTime
title: IDiscFormat2RawCDEventArgs::get_ElapsedTime (imapi2.h)
description: Retrieves the total elapsed time of the write operation. (IDiscFormat2RawCDEventArgs.get_ElapsedTime)
helpviewer_keywords: ["IDiscFormat2RawCDEventArgs interface [IMAPI]","get_ElapsedTime method","IDiscFormat2RawCDEventArgs.get_ElapsedTime","IDiscFormat2RawCDEventArgs::get_ElapsedTime","get_ElapsedTime","get_ElapsedTime method [IMAPI]","get_ElapsedTime method [IMAPI]","IDiscFormat2RawCDEventArgs interface","imapi.idiscformat2rawcdeventargs_get_elapsedtime","imapi2/IDiscFormat2RawCDEventArgs::get_ElapsedTime"]
old-location: imapi\idiscformat2rawcdeventargs_get_elapsedtime.htm
tech.root: imapi
ms.assetid: 87a1b606-f91b-4a14-b3b0-17d224d841fc
ms.date: 12/05/2018
ms.keywords: IDiscFormat2RawCDEventArgs interface [IMAPI],get_ElapsedTime method, IDiscFormat2RawCDEventArgs.get_ElapsedTime, IDiscFormat2RawCDEventArgs::get_ElapsedTime, get_ElapsedTime, get_ElapsedTime method [IMAPI], get_ElapsedTime method [IMAPI],IDiscFormat2RawCDEventArgs interface, imapi.idiscformat2rawcdeventargs_get_elapsedtime, imapi2/IDiscFormat2RawCDEventArgs::get_ElapsedTime
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
 - IDiscFormat2RawCDEventArgs::get_ElapsedTime
 - imapi2/IDiscFormat2RawCDEventArgs::get_ElapsedTime
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
 - IDiscFormat2RawCDEventArgs.get_ElapsedTime
---

# IDiscFormat2RawCDEventArgs::get_ElapsedTime


## -description

Retrieves the total elapsed time of the write operation.

## -parameters

### -param value [out]

Elapsed time, in seconds, of the write operation.

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

<a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents">DDiscFormat2RawCDEvents</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs">IDiscFormat2RawCDEventArgs</a>

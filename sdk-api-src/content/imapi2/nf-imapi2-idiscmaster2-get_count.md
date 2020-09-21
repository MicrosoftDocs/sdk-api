---
UID: NF:imapi2.IDiscMaster2.get_Count
title: IDiscMaster2::get_Count (imapi2.h)
description: Retrieves the number of the CD and DVD disc devices installed on the computer.
helpviewer_keywords: ["IDiscMaster2 interface [IMAPI]","get_Count method","IDiscMaster2.get_Count","IDiscMaster2::get_Count","get_Count","get_Count method [IMAPI]","get_Count method [IMAPI]","IDiscMaster2 interface","imapi.idiscmaster2_get_count","imapi2/IDiscMaster2::get_Count"]
old-location: imapi\idiscmaster2_get_count.htm
tech.root: imapi
ms.assetid: b1e0ec8f-4c66-4648-ad76-2998200ea574
ms.date: 12/05/2018
ms.keywords: IDiscMaster2 interface [IMAPI],get_Count method, IDiscMaster2.get_Count, IDiscMaster2::get_Count, get_Count, get_Count method [IMAPI], get_Count method [IMAPI],IDiscMaster2 interface, imapi.idiscmaster2_get_count, imapi2/IDiscMaster2::get_Count
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
 - IDiscMaster2::get_Count
 - imapi2/IDiscMaster2::get_Count
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
 - IDiscMaster2.get_Count
---

# IDiscMaster2::get_Count


## -description

Retrieves the number of the CD and DVD disc devices installed on the computer.

## -parameters

### -param value [out]

Number of CD and DVD disc devices installed on the computer.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified failure.

Value: 0x80004005

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2">IDiscMaster2</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscmaster2-get_item">IDiscMaster2::get_Item</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscmaster2-get__newenum">IDiscMaster::__NewEnum</a>
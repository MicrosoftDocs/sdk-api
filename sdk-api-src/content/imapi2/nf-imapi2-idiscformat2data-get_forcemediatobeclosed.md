---
UID: NF:imapi2.IDiscFormat2Data.get_ForceMediaToBeClosed
title: IDiscFormat2Data::get_ForceMediaToBeClosed (imapi2.h)
description: Determines if further additions to the file system are prevented. (Get)
helpviewer_keywords: ["IDiscFormat2Data interface [IMAPI]","get_ForceMediaToBeClosed method","IDiscFormat2Data.get_ForceMediaToBeClosed","IDiscFormat2Data::get_ForceMediaToBeClosed","get_ForceMediaToBeClosed","get_ForceMediaToBeClosed method [IMAPI]","get_ForceMediaToBeClosed method [IMAPI]","IDiscFormat2Data interface","imapi.idiscformat2data_get_forcemediatobeclosed","imapi2/IDiscFormat2Data::get_ForceMediaToBeClosed"]
old-location: imapi\idiscformat2data_get_forcemediatobeclosed.htm
tech.root: imapi
ms.assetid: 9de0afa9-93b7-4a12-b8e2-a9c083692f98
ms.date: 12/05/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],get_ForceMediaToBeClosed method, IDiscFormat2Data.get_ForceMediaToBeClosed, IDiscFormat2Data::get_ForceMediaToBeClosed, get_ForceMediaToBeClosed, get_ForceMediaToBeClosed method [IMAPI], get_ForceMediaToBeClosed method [IMAPI],IDiscFormat2Data interface, imapi.idiscformat2data_get_forcemediatobeclosed, imapi2/IDiscFormat2Data::get_ForceMediaToBeClosed
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
 - IDiscFormat2Data::get_ForceMediaToBeClosed
 - imapi2/IDiscFormat2Data::get_ForceMediaToBeClosed
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
 - IDiscFormat2Data.get_ForceMediaToBeClosed
---

# IDiscFormat2Data::get_ForceMediaToBeClosed


## -description

Determines if further additions to the file system are prevented.

## -parameters

### -param value [out]

Is VARIANT_TRUE if the next write session ends by marking the disc as closed to subsequent write sessions. Otherwise, VARIANT_FALSE to keep the disc open for subsequent write sessions.

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

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_forcemediatobeclosed">IDiscFormat2Data::put_ForceMediaToBeClosed</a>

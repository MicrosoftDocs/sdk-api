---
UID: NF:imapi2fs.IProgressItems.get_Count
title: IProgressItems::get_Count (imapi2fs.h)
description: Retrieves the number of progress items in the collection.
helpviewer_keywords: ["IProgressItems interface [IMAPI]","get_Count method","IProgressItems.get_Count","IProgressItems::get_Count","get_Count","get_Count method [IMAPI]","get_Count method [IMAPI]","IProgressItems interface","imapi.iprogressitems_get_count","imapi2fs/IProgressItems::get_Count"]
old-location: imapi\iprogressitems_get_count.htm
tech.root: imapi
ms.assetid: 370386fe-17b0-4cf3-9c28-880a85456e19
ms.date: 12/05/2018
ms.keywords: IProgressItems interface [IMAPI],get_Count method, IProgressItems.get_Count, IProgressItems::get_Count, get_Count, get_Count method [IMAPI], get_Count method [IMAPI],IProgressItems interface, imapi.iprogressitems_get_count, imapi2fs/IProgressItems::get_Count
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
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
 - IProgressItems::get_Count
 - imapi2fs/IProgressItems::get_Count
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IProgressItems.get_Count
---

# IProgressItems::get_Count


## -description

Retrieves the number of progress items in the collection.

## -parameters

### -param Count [out]

Number of progress items in the collection.

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

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems">IProgressItems</a>
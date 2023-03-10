---
UID: NF:imapi2fs.IEnumFsiItems.Skip
title: IEnumFsiItems::Skip (imapi2fs.h)
description: Skips a specified number of items in the enumeration sequence. (IEnumFsiItems.Skip)
helpviewer_keywords: ["IEnumFsiItems interface [IMAPI]","Skip method","IEnumFsiItems.Skip","IEnumFsiItems::Skip","Skip","Skip method [IMAPI]","Skip method [IMAPI]","IEnumFsiItems interface","imapi.ienumfsiitems_skip","imapi2fs/IEnumFsiItems::Skip"]
old-location: imapi\ienumfsiitems_skip.htm
tech.root: imapi
ms.assetid: f1bf8542-12b9-4228-9e0e-1defbb57cac3
ms.date: 12/05/2018
ms.keywords: IEnumFsiItems interface [IMAPI],Skip method, IEnumFsiItems.Skip, IEnumFsiItems::Skip, Skip, Skip method [IMAPI], Skip method [IMAPI],IEnumFsiItems interface, imapi.ienumfsiitems_skip, imapi2fs/IEnumFsiItems::Skip
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
 - IEnumFsiItems::Skip
 - imapi2fs/IEnumFsiItems::Skip
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
 - IEnumFsiItems.Skip
---

# IEnumFsiItems::Skip


## -description

Skips a specified number of items in the enumeration sequence.

## -parameters

### -param celt [in]

Number of items to skip.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Skipped less than the number of requested elements.

</td>
</tr>
</table>

## -remarks

If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems">IEnumFsiItems</a>

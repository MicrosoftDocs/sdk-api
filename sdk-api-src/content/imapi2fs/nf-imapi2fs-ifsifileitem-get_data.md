---
UID: NF:imapi2fs.IFsiFileItem.get_Data
title: IFsiFileItem::get_Data (imapi2fs.h)
description: Retrieves the data stream of the file's content.
helpviewer_keywords: ["IFsiFileItem interface [IMAPI]","get_Data method","IFsiFileItem.get_Data","IFsiFileItem::get_Data","get_Data","get_Data method [IMAPI]","get_Data method [IMAPI]","IFsiFileItem interface","imapi.ifsifileitem_get_data","imapi2fs/IFsiFileItem::get_Data"]
old-location: imapi\ifsifileitem_get_data.htm
tech.root: imapi
ms.assetid: 90ed4c81-7113-4329-ae1e-9114740b7e09
ms.date: 12/05/2018
ms.keywords: IFsiFileItem interface [IMAPI],get_Data method, IFsiFileItem.get_Data, IFsiFileItem::get_Data, get_Data, get_Data method [IMAPI], get_Data method [IMAPI],IFsiFileItem interface, imapi.ifsifileitem_get_data, imapi2fs/IFsiFileItem::get_Data
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
 - IFsiFileItem::get_Data
 - imapi2fs/IFsiFileItem::get_Data
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
 - IFsiFileItem.get_Data
---

# IFsiFileItem::get_Data


## -description

Retrieves the data stream of the file's content.

## -parameters

### -param pVal [out]

An <b>IStream</b> interface of the contents of the file.

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
Failed to allocate necessary memory.

Value: 0x8007000E

</td>
</tr>
</table>

## -remarks

The contents of the file becomes read-only once the file item is added to file system image.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem">IFsiFileItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsifileitem-put_data">IFsiFileItem::put_Data</a>
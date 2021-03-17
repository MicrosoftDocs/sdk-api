---
UID: NF:imapi2fs.IFsiFileItem.put_Data
title: IFsiFileItem::put_Data (imapi2fs.h)
description: Sets the data stream of the file's content.
helpviewer_keywords: ["IFsiFileItem interface [IMAPI]","put_Data method","IFsiFileItem.put_Data","IFsiFileItem::put_Data","imapi.ifsifileitem_put_data","imapi2fs/IFsiFileItem::put_Data","put_Data","put_Data method [IMAPI]","put_Data method [IMAPI]","IFsiFileItem interface"]
old-location: imapi\ifsifileitem_put_data.htm
tech.root: imapi
ms.assetid: 5fe00500-615c-48fe-a4a3-b3291e61db1f
ms.date: 12/05/2018
ms.keywords: IFsiFileItem interface [IMAPI],put_Data method, IFsiFileItem.put_Data, IFsiFileItem::put_Data, imapi.ifsifileitem_put_data, imapi2fs/IFsiFileItem::put_Data, put_Data, put_Data method [IMAPI], put_Data method [IMAPI],IFsiFileItem interface
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
 - IFsiFileItem::put_Data
 - imapi2fs/IFsiFileItem::put_Data
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
 - IFsiFileItem.put_Data
---

# IFsiFileItem::put_Data


## -description

Sets the data stream of the file's content.

## -parameters

### -param newVal [in]

An <b>IStream</b> interface of the content of the file to add to the file system image.

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
<dt><b>IMAPI_E_READONLY</b></dt>
</dl>
</td>
<td width="60%">
FileSystemImage object is in read only mode.

Value: 0xC0AAB102

</td>
</tr>
</table>

## -remarks

The contents of the file becomes read-only once the file item is added to file system image.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem">IFsiFileItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsifileitem-get_data">IFsiFileItem::get_Data</a>
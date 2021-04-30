---
UID: NF:imapi2fs.IFsiDirectoryItem.get_Count
title: IFsiDirectoryItem::get_Count (imapi2fs.h)
description: Number of child items in the enumeration.
helpviewer_keywords: ["IFsiDirectoryItem interface [IMAPI]","get_Count method","IFsiDirectoryItem.get_Count","IFsiDirectoryItem::get_Count","get_Count","get_Count method [IMAPI]","get_Count method [IMAPI]","IFsiDirectoryItem interface","imapi.ifsidirectoryitem_get_count","imapi2fs/IFsiDirectoryItem::get_Count"]
old-location: imapi\ifsidirectoryitem_get_count.htm
tech.root: imapi
ms.assetid: 66553025-35c9-4902-a184-01c07a478977
ms.date: 12/05/2018
ms.keywords: IFsiDirectoryItem interface [IMAPI],get_Count method, IFsiDirectoryItem.get_Count, IFsiDirectoryItem::get_Count, get_Count, get_Count method [IMAPI], get_Count method [IMAPI],IFsiDirectoryItem interface, imapi.ifsidirectoryitem_get_count, imapi2fs/IFsiDirectoryItem::get_Count
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
 - IFsiDirectoryItem::get_Count
 - imapi2fs/IFsiDirectoryItem::get_Count
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
 - IFsiDirectoryItem.get_Count
---

# IFsiDirectoryItem::get_Count


## -description

Number of  child items in the enumeration.

## -parameters

### -param Count [out]

Number of directory and file items within the directory in the file system image.

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

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem">IFsiDirectoryItem</a>



<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem">IFsiFileItem</a>
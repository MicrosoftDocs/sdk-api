---
UID: NF:imapi2fs.IProgressItem.get_Description
title: IProgressItem::get_Description (imapi2fs.h)
description: Retrieves the description in the progress item.
helpviewer_keywords: ["IProgressItem interface [IMAPI]","get_Description method","IProgressItem.get_Description","IProgressItem::get_Description","get_Description","get_Description method [IMAPI]","get_Description method [IMAPI]","IProgressItem interface","imapi.iprogressitem_get_description","imapi2fs/IProgressItem::get_Description"]
old-location: imapi\iprogressitem_get_description.htm
tech.root: imapi
ms.assetid: 72da165f-a875-4f26-a2ba-701ad0a4a9d1
ms.date: 12/05/2018
ms.keywords: IProgressItem interface [IMAPI],get_Description method, IProgressItem.get_Description, IProgressItem::get_Description, get_Description, get_Description method [IMAPI], get_Description method [IMAPI],IProgressItem interface, imapi.iprogressitem_get_description, imapi2fs/IProgressItem::get_Description
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
 - IProgressItem::get_Description
 - imapi2fs/IProgressItem::get_Description
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
 - IProgressItem.get_Description
---

# IProgressItem::get_Description


## -description

Retrieves the description in the progress item.

## -parameters

### -param desc [out]

String containing the description. The description contains the name of the file in the file system image.

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

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem">IProgressItem</a>
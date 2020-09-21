---
UID: NF:imapi2fs.IFsiItem.put_CreationTime
title: IFsiItem::put_CreationTime (imapi2fs.h)
description: Sets the date and time that the directory or file item was created and added to the file system image.
helpviewer_keywords: ["IFsiItem interface [IMAPI]","put_CreationTime method","IFsiItem.put_CreationTime","IFsiItem::put_CreationTime","imapi.ifsiitem_put_creationtime","imapi2fs/IFsiItem::put_CreationTime","put_CreationTime","put_CreationTime method [IMAPI]","put_CreationTime method [IMAPI]","IFsiItem interface"]
old-location: imapi\ifsiitem_put_creationtime.htm
tech.root: imapi
ms.assetid: 242e6f68-d9bc-4881-adf3-22d7b32a1dfe
ms.date: 12/05/2018
ms.keywords: IFsiItem interface [IMAPI],put_CreationTime method, IFsiItem.put_CreationTime, IFsiItem::put_CreationTime, imapi.ifsiitem_put_creationtime, imapi2fs/IFsiItem::put_CreationTime, put_CreationTime, put_CreationTime method [IMAPI], put_CreationTime method [IMAPI],IFsiItem interface
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
 - IFsiItem::put_CreationTime
 - imapi2fs/IFsiItem::put_CreationTime
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
 - IFsiItem.put_CreationTime
---

# IFsiItem::put_CreationTime


## -description

Sets the date and time that the  directory or file item was created and added to the file system image.

## -parameters

### -param newVal [in]

Date and time that the directory or file item was created and added to the file system image, according to UTC time. Defaults to the time the item was added to the image.

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
<dt><b>IMAPI_E_READONLY</b></dt>
</dl>
</td>
<td width="60%">
FileSystemImage object is in read only mode.

Value: 0xC0AAB102

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

IMAPI does not support the extended attribute for <i>CreationTime</i>, and as a result, UDFS populates the <i>CreationTime</i> with the value expressed by the <i>LastAccessed</i> property from the file entry.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem">IFsiItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-get_creationtime">IFsiItem::get_CreationTime</a>
---
UID: NF:imapi2fs.IFsiItem.get_Name
title: IFsiItem::get_Name (imapi2fs.h)
description: Retrieves the name of the directory or file item in the file system image.
helpviewer_keywords: ["IFsiItem interface [IMAPI]","get_Name method","IFsiItem.get_Name","IFsiItem::get_Name","get_Name","get_Name method [IMAPI]","get_Name method [IMAPI]","IFsiItem interface","imapi.ifsiitem_get_name","imapi2fs/IFsiItem::get_Name"]
old-location: imapi\ifsiitem_get_name.htm
tech.root: imapi
ms.assetid: 4cb6e270-6bbf-414f-a9ed-b290da3dafe9
ms.date: 12/05/2018
ms.keywords: IFsiItem interface [IMAPI],get_Name method, IFsiItem.get_Name, IFsiItem::get_Name, get_Name, get_Name method [IMAPI], get_Name method [IMAPI],IFsiItem interface, imapi.ifsiitem_get_name, imapi2fs/IFsiItem::get_Name
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
 - IFsiItem::get_Name
 - imapi2fs/IFsiItem::get_Name
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
 - IFsiItem.get_Name
---

# IFsiItem::get_Name


## -description

Retrieves the name of the directory or file item in the file system image.

## -parameters

### -param pVal [out]

String that contains the name of the file or directory item in the file system image.

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

## -remarks

To get the full path to the item, call the <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-get_fullpath">IFsiItem::get_FullPath</a> method.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem">IFsiItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-get_fullpath">IFsiItem::get_FullPath</a>